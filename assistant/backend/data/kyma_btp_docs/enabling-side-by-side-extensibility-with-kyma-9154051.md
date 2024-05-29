

# Enabling Side-by-Side Extensibility with Kyma

> ### Note:  
> The content in this section is not relevant for China \(Shanghai\) and Government Cloud \(US\) regions.

You want to extend the functionality on top of your existing SAP solution because your specific business needs require it. You also want to use the SAP BTP Kyma environment. You can build an extension application that contains your business logic and UI changes and deploy it in SAP BTP Kyma runtime. For the users of your SAP solution, this change will be seamless, it will look as if it's part of the original functionality. At the same time, you can use the extension capabilities of SAP BTP to implement the additional workflows or modules. This is called side-by-side extensibility wth Kyma.

To enable the side-by-side extensibility with Kyma for your SAP solution, you have to create an SAP BTP Kyma environment instance in your subaccount in SAP BTP. Then, you have to connect the corresponding SAP system with the global account in SAP BTP. Use the automated configurations for the following SAP solutions:

-   [Extending SAP S/4HANA Cloud in the Cloud Foundry and Kyma Environment](extending-sap-s-4hana-cloud-in-the-cloud-foundry-and-kyma-environment-40b9e6c.md)

-   [Extending SAP Marketing Cloud in the Cloud Foundry and Kyma Environment](extending-sap-marketing-cloud-in-the-cloud-foundry-and-kyma-environment-18bb3d9.md)

-   [Extending SAP SuccessFactors in the Cloud Foundry and Kyma Environment](extending-sap-successfactors-in-the-cloud-foundry-and-kyma-environment-9e33934.md)

-   [Extending SAP Customer Experience Products in the Kyma Environment](extending-sap-customer-experience-products-in-the-kyma-environment-83df31a.md)


Finally, you can create a formation of type *Side-by-Side Extensibility with Kyma* where you can include one or more SAP systems depending on your use case.

