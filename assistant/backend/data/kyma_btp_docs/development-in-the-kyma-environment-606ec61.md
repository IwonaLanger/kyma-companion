

# Development in the Kyma Environment

Learn more about developing applications in the Kyma environment.





## Overview

The [Kyma Environment](kyma-environment-468c2f3.md) enables you to build simple Functions, develop, and deploy more complex microservices, or mixtures of those, depending on your use case complexity level. Both, Functions and microservices, can act as stand-alone applications or extensions of these SAP systems:

-   SAP S/4HANA

-   SAP S/4HANA Cloud

-   SAP S/4HANA Cloud, public edition

-   SAP Field Service Management

-   SAP SuccessFactors

-   SAP Customer Experience systems:

    -   SAP Commerce Cloud

    -   SAP Cloud for Customer

    -   SAP Marketing Cloud







## Language of Choice

With the Kyma environment, you can create microservices in the language of your choice and run them as containerized applications. Additionally, you can create Functions in Node.js or Python.





## Kyma Dashboard and kubectl

The Kyma environment comes with a central administration dashboard \(Kyma dashboard\), which allows you to deploy microservices, create Functions, and manage their configurations. You can also use it to connect SAP BTP services to your cluster and manage them using SAP BTP Service Operator, create instances of these services, and use them in your microservices or Functions.

For those who prefer to work with command-line tools, the Kyma environment also offers the Kubernetes command-line tool, kubectl.





## SAP Cloud Application Programming Model

The SAP Cloud Application Programming Model \(CAP\) is the recommended framework for application and service development in the Kyma environment. To learn more, see [SAP Cloud Application Programming Model](sap-cloud-application-programming-model-042061d.md).





## Using API

The Kyma and third-party modules' APIs may vary from the least stable alpha version through a more stable beta and the most stable **vX** version \(**X** being an integer\). While using the alpha version, you can face issues with module upgrades, as there is no guarantee that the API will not change or won’t be removed in the future. For more information, check the [Kubernetes API versioning](https://kubernetes.io/docs/reference/using-api/#api-versioning).

Run this command to get the list of the APIs, their kind, and version:

```
kubectl get crd -o custom-columns="KIND:.spec.names.kind,GROUP:.spec.group,VERSION:.spec.versions[*].name
```

If an API is available in two versions, always use the version that is more stable.





## Development Tutorials

To help you get started with the development process, go through the set of tutorials that show how to [develop a full-stack application](https://developers.sap.com/mission.cp-kyma-full-stack.html) in the Kyma environment. You'll create a sample containerized microservice, learn how to expose it via API, and trigger it with events. Additionally, you create Functions as well as instances of external services that you can use in your microservices and Functions.

-   [Deploy MSSQL in the Kyma Environment](https://developers.sap.com/tutorials/cp-kyma-mssql-deployment.html)

-   [Deploy a Go MSSQL API Endpoint in the Kyma Environment](https://developers.sap.com/tutorials/cp-kyma-api-mssql-golang.html)

-   [Deploy the SAPUI5 Frontend in the Kyma Environment](https://developers.sap.com/tutorials/cp-kyma-frontend-ui5-mssql.html)

-   [Trigger a Microservice with an Event](https://developers.sap.com/tutorials/cp-kyma-microservice-trigger.html)

-   [Use Redis in the Kyma Environment to Store and Retrieve Data](https://developers.sap.com/tutorials/cp-kyma-redis-function.html)






## Related Information

-   [Extension Samples](https://github.com/SAP-samples/kyma-runtime-extension-samples)

    Kyma provides a ready-to-use project that contains sample applications. You can take advantage of them to build event- and API-based extensions in the Kyma environment using your favorite technology. These samples are implemented in multiple languages and demonstrate various Kyma environment features and use case scenarios.

-   [Using SAP BTP Services in the Kyma Environment](using-sap-btp-services-in-the-kyma-environment-ea4dd81.md#loioea4dd81e49254dd482d32e3c20f4477a)

    Kyma environment allows you to extend the SAP systems to build and deploy your own applications.

-   [Deploy Workloads in the Kyma Environment to Extend SAP Systems](deploy-workloads-in-the-kyma-environment-to-extend-sap-systems-fe4ba5b.md)

    Access the Kyma environment and start creating extensions for SAP systems using Functions.


