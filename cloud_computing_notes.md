## What is Cloud Computing?

1. A model for enabling convenient, on-demand network access to a shared pool of configurable computing:
    Network
    Servers
    Storage
    Applications
    Services
2. Can be rapidly provisioned and released with minimal management effort
3. Provides high levels of abstractions from computation to Storage
4. Basically hard drives, databases or CPUs served to us on demand.
5. Has some essential characteristics, service models and deployment models.

## Essential characteristics of Cloud Computing:

1. On-demand self-service
2. Heterogenous access(available anytime from anywhere)
3. Resource Pooling
4. Measured access
5. High availability at all times

## Why we need cloud Computing?
1. Flexibility (can be easily scaled up and down and also pay per use)
2. Disaster-Recovery
3. Automatic software updates
4. No Large Up-front investment
5. Increased Collaboration
6. Working from anywhere
7. Document Control
8. Security
9. Competitiveness
10. Environment friendly

## Service Models in the Cloud 
1. Software as a Service(SaaS)
    Provides consumer the capability to use the provider's application running on a cloud infrastructure.
    Applications are accessible from various client devices such as web browser, a mobile phone or tablet
    Examples: Webmail, skype, facetime or whatsapp , Office365 etc.
    Consumer does not manage or control the underlying cloud infrastructure.

2. Platform as a Service(PaaS)
    Provides the consumer the capability to deploy onto the cloud infrastructure consumer created or acquired applications       developed using programming languages and tools supported by the provider.
    Consumer does not manage or control the underlying cloud infrastructure.
    Consumer has control over the deployed applications and possibly application hosting environment configurations.
    Example: Cloud Foundry, Microsoft Azure and Google cloud
    
 ### What is a platform?
  Anything you leverage to accomplish a task.
  You dont have to start from scratch.
  Well known software platforms are Windows and MAC OS.
    
 ### What is Paas?
  With PaaS you don't have to deal with hardware or software in most situations.
  Providers deliver everything from Servers to Runtime for your application.

 ### Goal of a PaaS?
   The ultimate goal of a PaaS is to make it easier for you to run your website or web application
   no matter how much traffic it gets.
   You just deploy your application and the service figures out what to do with it.
   A Paas should handle scaling seamlessly for you so you can just focus on your website and the code running it.
  Some PaaS Providers: CloudFoundry, AWS , GCP, IBM Bluemix, Microsoft Azure, SAP with HANA Clould platform

   
3. Infrastructure as a Service(IaaS)
    
    
## 12 Factor apps

1. Code is version controlled so that you can easily deploy your code to different environments like Dev, staging and prod.

2. Dependencies are declared and isolated. Dependencies can be libraries, tools or databases.
    Your application should not assume that all these dependencies will be available in the target environment.
    Instead of assuming everything should be there you must declare your dependencies in a manifest file that has the power     to bring everything you need together.

3. Configuration is stored in the environment.
    Example your database configuration should not be in a static file in your application instead it should be done in your     environment.

4. Backing services as attached resources.
    Application can have lot of services like Databases, Queuing, Caching, webservices that it uses and all of them are         accessed over the network.
    These are no different then those you have in your local environment. This kind of treatment allows you to have your         dependencies decoupled and more importantly you can attach and detach resources at will.
    Only changes will be to your environment variables depending on the environment you are running in.

5. Build and Run Stages are Separate
    You should be able to build and deploy your application to staging and prod environment seamlessly and completely           separated.

6. Application executed as Stateless Processes
    You should never assume that state or processes are part of your application.

7. Services are Exported via Port Binding
    Your application must be completely self contained. It shouldn't rely on a specific webserver or a port. So you should       be listening on a very specific port and not on port 8080 or 4044. 
    This is because these ports can be used for anything from a caching server to a queueing mechanism.
    You simply cant rely on that.

8. Applications Scaled out via Process Model
    Processes must be embraced as first class citizens in your application because they simply do everything. You have           processes for listening to queues, making HTTP requests and listening to incoming requests.
    These are all handled by individual processes. So if you assume that your application grows much much bigger then they       are going to need more processing power and memory.
    But vertical scaling is limited. You have to be scaling horizontally and that means you have to increase the number of       workers for certain tasks such as making requests or removing server. 
    For doing such scaling OS process managers are well designed to take care of such tasks.

9. Processes are disposable
    minimal start up time and graceful shutdown are the key here. So when applications crash you want them to recover and be    up quickly.

10. Parity between Application environments
    Design for a continous deployment pipeline. Allows to go to production quickly.
    
11. Logs treated as Event streams
    Treat logs as event streams since they carry important information regarding our application state.
    Application should not bother about logs and logging framework should take care of them.

12. Management tasks run as one off Processes
    Management tasks are important part of an application to maintain or upgrade it. We should be using identical               environments for running them.

    










