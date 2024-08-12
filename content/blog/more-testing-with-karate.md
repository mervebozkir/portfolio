---
title: "Web Service Testing with Karate DSL"
dateString: Jul 2021
draft: false
tags: ["Karate DSL", "API Testing", "BDD"]
weight: 101
cover:
    image: "blog/what-is-karate-testing/karate-test-header.jpg"
---

# Introduction

In the previous article, we talked about creating a project with Karate and created a small test. Now, let's try to create some more detailed test examples.

# Testing

For our first example, let's look at [API examples on GitHub.](https://github.com/public-apis/public-apis) On the opened page, under the Public APIs heading, we can click on the Animals option or scroll down to reach the same heading.

I selected the [IUCN Red List of Threatened Species](http://apiv3.iucnredlist.org/api/v3/docs) example from the Animals API examples. You can also continue with a different example. When we click the link, we get examples for the International Union for Conservation of Nature Red List of Threatened Species.

For our first example, let's open our project in the IntelliJ application again.

* First, let's call the service that lists the isocodes of countries. We specify the URL information of the address we need to go to http://apiv3.iucnredlist.org/api/v3/country/list?token='YOUR-TOKEN' in the background.

*In Karate tests, the background is the area where we use common definitions and is executed before every test.*

We can also specify the URL information on the scenario, but it will be better to specify it in the background since we will use it in multiple scenarios.

![](/blog/more-testing-with-karate/k-test-1.png)

Afterwards, we can start defining the path we will use in our scenario.

![](/blog/more-testing-with-karate/k-test-2.png)

In this way, we have specified the service we want to call. Before proceeding, we can run our test once to check if the access is provided.

![](/blog/more-testing-with-karate/k-test-3.png)

We can see from the test result that access to the specified address is provided.

The service address we want to access was http://apiv3.iucnredlist.org/api/v3/country/list?token='YOUR-TOKEN'. Here, the token definition that comes after the question mark is the parameter value expected by the service. Parameter information in Karate scenarios is specified as shown below.

![](/blog/more-testing-with-karate/k-test-4.png)

Afterwards, we complete our test steps by specifying our method and the status we expect, and by printing the response.

![](/blog/more-testing-with-karate/k-test-5.png)

When we run our test, we see that information for 251 countries is listed.

![](/blog/more-testing-with-karate/k-test-6.png)

Here, the results content is sent as an array. We can retrieve the desired element from this array by specifying its index number.

Before printing the element in the array, I printed "example" to make it easier to distinguish in the printed response. Then, to access the elements inside the array, I specified response.results and then the index number of the element I wanted to retrieve.

![](/blog/more-testing-with-karate/k-test-7.png)

In this way, we can view the value of the element printed in the response as shown below.

![](/blog/more-testing-with-karate/k-test-8.png)

* Let's try calling a different service. Since we defined the URL in the background, we can create a different scenario by just changing the path.

![](/blog/more-testing-with-karate/k-test-10.png)

When we run the feature in this way, we can see that both scenarios work successfully.

* In Karate, we can use the **match** command to check whether the fields returned in the response are equal to the values we want. In our second scenario, there is also a response returned as an array.

![](/blog/more-testing-with-karate/k-test-11.png)

Here, let's perform a check on the response. For this, we should first access the results in the response and then the field we want to check within the array. Let's check that the scientific name value of the fourth element in the array is equal to "Abies nordmanniana".

![](/blog/more-testing-with-karate/k-test-12.png)

In this way, we can ensure the control of the field returned in the response. If we write something different on the right side, we can also see this in our test result.

![](/blog/more-testing-with-karate/k-test-13.png)

When we run the test after making the change, we can see that the value we expect and the value returned in the response are not equal.

![](/blog/more-testing-with-karate/k-test-14.png)

Let's continue with the post method.

* In Karate, we can specify our requests within the scenario steps or call them from outside.

If we want to call it within the scenario step, we can write it as shown below.

![](/blog/more-testing-with-karate/k-test-15.png)

However, I prefer to call my request from outside because specifying it within the test step can make it difficult to track when there are too many fields in the request.

To call our request from outside, we need to create a separate file first. We can do this by right-clicking on the folder where our feature file is located and following the New-> File step. Since we use JSON in our tests, we create our request file with the '.json' extension.

![](/blog/more-testing-with-karate/k-test-16.png)

After creating my request in this way, I need to call this request within my test. I do this with the **read** command.

![](/blog/more-testing-with-karate/k-test-17.png)

Then, by specifying my method and the status I expect, and by printing the response, I complete my test.

![](/blog/more-testing-with-karate/k-test-18.png)

After running our test, we can see our result as shown below.

![](/blog/more-testing-with-karate/k-test-19.png)

* If we want to make changes to the request file we use, we can use the **set** command.

![](/blog/more-testing-with-karate/k-test-20.png)

After setting it up in this way, we can print our new request and see it.

![](/blog/more-testing-with-karate/k-test-21.png)

When we run our test, we can see both our request and our response.

Request:

![](/blog/more-testing-with-karate/k-test-22.png)

Response:

![](/blog/more-testing-with-karate/k-test-23.png)

We did not make any changes to the content of our user.json file while doing this. With the **set** command, we can also make dynamic changes to our request.

I hope my article, where I mentioned the basic steps of web service testing with Karate, will be useful to the readers. 😊

*SOURCES*

- https://github.com/public-apis/public-apis?source=post_page-----d606862d38a9--------------------------------
- https://reqres.in/?source=post_page-----d606862d38a9--------------------------------

[Medium](https://medium.com/@mervebozkir/karate-i%CC%87le-web-servi%CC%87s-testleri%CC%87-d606862d38a9)