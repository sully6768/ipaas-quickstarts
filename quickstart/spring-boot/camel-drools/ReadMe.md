# Spring-Boot Camel-Drools QuickStart

This example demonstrates how you can use Apache Camel and Drools with Spring Boot
based on a [fabric8 Java base image](https://github.com/fabric8io/base-images#java-base-images)

DRL files contain simple rules which are used to create knowledge session via Spring configuration file.
Camel routes, defined via Spring as well, are then used to e.g. pass (insert) the Body of the message as a POJO to Drools engine for execution.

### Building

The example can be built with

    mvn clean install


### Running the example locally

The example can be run locally using the following Maven goal:

    mvn spring-boot:run


### Running the example in fabric8

It is assumed a running Kubernetes platform is already running. If not you can find details how to [get started](http://fabric8.io/guide/getStarted/index.html).

The example can be built and deployed using a single goal:

    mvn -Pf8-local-deploy

When the example runs in fabric8, you can use the OpenShift client tool to inspect the status

To list all the running pods:

    oc get pods

Then find the name of the pod that runs this quickstart, and output the logs from the running pods with:

    oc logs <name of pod>

You can also use the fabric8 [web console](http://fabric8.io/guide/console.html) to manage the
running pods, and view logs and much more.


### More details

You can find more details about running this [quickstart](http://fabric8.io/guide/quickstarts/running.html) on the website. This also includes instructions how to change the Docker image user and registry.
