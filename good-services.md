## What makes a Good Service?
Focus on two key concepts: *loose coupling* and *high cohesion*. 

#### Loose Coupling
Where services are loosely coupled, a change to one service should not require a change to another. The whole point of a microservice is being able to make a change to one service and deploy it, without needing to change any other part of the system. This is really quite important.

What sort of things cause tight coupling? A classic mistake is to pick an integration style that tightly binds one service to another, causing changes inside the serivce to require a change to consumers.

A loosely coupled service knows as little as it needs to about the serivces with which it collaborates. This also means we probably want to limit the number of different types of calls from one service to another, because the potential performance problem, chatty communication can lead to tight coupling.

#### High Cohesion
WE want related behavior to sit together, and unrelated behavior to sit elsewhere. Why? Well, if we want to change behavior, we want to be able to change it in one place, and release that change as soon as possible. If we have to change that behavior in lots of different places, we'll have to release lots of different services (perhaps at the same time) to deliver that change. Making changes in lots of different places is slower, and deploying lots of services at once is risky; both of which we want to avoid.

So we want t ofind boundaries within our problem domain that help ensure that related behavior is in one place, and that communicate with otehr boundaries as loosely as possible.