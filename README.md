Retrofit is a type-safe HTTP client for Android and Java — developed by Square who developed Dagger, Okhttp, etc.

In this article, we’re going to explain how to use Retrofit, with a focus on its most interesting features. More notably we’ll discuss the synchronous and asynchronous API, how to use it with authentication, logging, and some good modeling practices.

Table content:
Adding dependency
API Modeling and annotations
Make Retrofit Builder for Synchronous/Asynchronous API and different converters
Observe API Data in the ViewModel
Making a Reusable ApiInstance Class
Authentication
Logging

Build model classes from response.

Retrofit works by modeling over a base URL and by making interfaces return the entities from the REST endpoint.

For simplicity purposes we’re going to take a small part of the JSON by modeling our data class

We can see that we’re only taking a subset of properties for this example. Retrofit won’t complain about missing properties — since it only maps what we need, it won’t even complain if we were to add properties that are not in the JSON.
