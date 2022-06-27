Cloudfoundry
============

### Concept:

*   Opensource PAAS for cloud native development
    *   Cloud Infrastructure refreshment:  
        ![](/download/attachments/1029144608/image2022-6-27_10-35-38.png?version=1&modificationDate=1656318938288&api=v2)
*   Minimize developer effort on infrastructure  
    ![](/download/thumbnails/1029144608/image2022-6-27_10-15-34.png?version=1&modificationDate=1656317734120&api=v2)

### [CF vs k8s](https://tutorials.cloudfoundry.org/cf-and-k8s/docs/comparing/)

Differences focused on the abstraction leve. Some points:

Design & Built in Functionality:

*   cf: opinionated set of components
*   k8s: flexible set of systems

Exposed Complexity:

*   cf: hides implementation details
*   k8s: hides nothing

Personas:

*   Cloud Foundry has different user experiences for operators and for application developers
*   Kubernetes presents the same user interface for all its users

### [When to use cf?](https://tutorials.cloudfoundry.org/cf-and-k8s/docs/when-should-i-use-cloud-foundry/)

*   developers to have a**simplified experience**, and not need to learn all the details of Kubernetes
*   **secure defaults**that prevent privileged workloads from running
*   secure**multi-tenancy**by default
*   **patch images without developer involvement**

**[Apps on cf](https://tutorials.cloudfoundry.org/cf-and-k8s/docs/running-apps-on-cloud-foundry/)**

*   Write the app
*   Build a container image
    *   During staging, cf creates a reusable container image using buildpacks (like [packeto](https://paketo.io/))
*   Enable https access
*   Connect to dataservices 
    *   **Show marketplace services**
    *   **Create services**
    *   **Bind services**
*   **Later keep it running, apply logs, make it resilient, patch**

  

Links:

*   [What is cf?](https://tutorials.cloudfoundry.org/what-is-cf/docs/what-is-cf/)
*   [Cloudfoundry explained](https://www.youtube.com/watch?v=oUpqXxmr6oU)
*   [Cloudfoundry - Quick intro | Tech Primers](https://www.youtube.com/watch?v=vzSuYab2q5M)

  

Buildpacks
==========

*   A buildpack is a set of executables that inspects your app source code and creates a plan to build and run your application.
*   Check your app and determine what dependencies to download and how to configure the apps to communicate with bound services
*   [Packeto](https://paketo.io/) buildpacks transform apps source code into container images

Links:  
  

*   [What is Buildpack in PCF?](https://www.youtube.com/watch?v=Mo14JCWcotk)
*   [cf docs: Buildpacks](https://docs.cloudfoundry.org/buildpacks/)
*   [Buildpacks ](https://buildpacks.cloudfoundry.org/#/buildpacks)

MINIO
=====

*   Powered by Kubernetes, MinIO delivers scalable, secure, S3 compatible object storage to every public cloud.
*   Key concept:
    *   it does object storage
    *   k8s native
*   Can create standalone object storage self hosted and later compatible with public cloudes.  
    
*   Example done:  
    ![](/download/attachments/1029144608/image2022-6-27_17-10-32.png?version=1&modificationDate=1656342632405&api=v2)  
    

Links:

*   [MinIO](https://min.io/)
*   [Deploy a standalone MinIO](https://www.youtube.com/watch?v=dIQsPCHvHoM)

  

Epinio
======

*   Good explanation of the push process [here](https://docs.epinio.io/explanations/detailed-push-process)