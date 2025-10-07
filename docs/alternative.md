# TechXChange 2025 - Lab 2663 - Alternative Path (Read Only)

## Implement your changes (read only path)

To start with the implementation you would now clone the project into your local development environment.
To do this you use the k5 Solution CLI, our command-line interface, to pull the code into your development environment and to generate the boilerplate code based on the design files.

In our example, the distinction between CustomerOrder and InternalOrder was introduced as well as the orderType enum to differentiate between the two in the API. The API of another service got added as an integration namespace as well. For all of the above changes, the boilerplate code needed will be generated for us.

As soon as we clone the project, code generation begins and creates new files based on the design files.

### Auto-generated files
Since we added two new entities, each with a factory and instance commands, two new files, CustomerOrderCommand.java and InternalOrderCommand.java, were created. The files contain the auto-generated classes with the empty methods.

The other changes we made are also reflected in our project. The PostMail.java got generated to integrate the external API.

Everything from properties to methods of the classes are generated and ready to use in your business logic.

### Before implementation

You can take a look at [ORDERCOTXC01 | Before implementation](https://edu-gitlab.apps.openshift-01.knowis.cloud/techxchange25/ordercotxc01) to see the project after the code generation but before implementation.
As we only made the changes in the designer and haven't adjusted our code yet, you can see the implementation of the createOrder method before our changes in the src/main/java/com/k5/ordercotxc01/domain/ord/command/OrderCommand.java file. You can also see the boilerplate code generated for src/main/java/com/k5/ordercotxc01/domain/ord/command/CustomerOrderCommand.java and src/main/java/com/k5/ordercotxc01/domain/ord/command/InternalOrderCommand.java.

You can also take a look at the src/main/java/com/knowis/ordercotxc01/integration/email/service/PostMail.java file to see the generated file for the integrated service.

Take a few moments to explore the project and then continue with the finished project.

### After implementation

You can see the finished project with all the changes at [ORDERCOTXC02 | After implementation](https://edu-gitlab.apps.openshift-01.knowis.cloud/techxchange25/ordercotxc02).
We now differentiate between internal and customer orders in the src/main/java/com/k5/ordercotxc02/domain/ord/command/OrderCommand.java file and the src/main/java/com/knowis/ordercotxc02/integration/email/service/PostMail.java implementation got added.

We also changed the implementation of the src/main/java/com/k5/ordercotxc02/api/v1/OrdersApiV1Provider.java to send a confirmation email only to external customers.

### Additional information

To learn more about the code-generation, the implementation of the order command and the orders API you can visit [Learning Center | Implement commands](https://learning-devops-solution-workbench.knowis.cloud/docs/training/domainService/implement-commands/) and [Learning Center | Implement API operation](https://learning-devops-solution-workbench.knowis.cloud/docs/training/domainService/implement-api-operation/). You can also take a look at the other units in the Learning Center to learn more about the IBM DevOps Solution Workbench.
