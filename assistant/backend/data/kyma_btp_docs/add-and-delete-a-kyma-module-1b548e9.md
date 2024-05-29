

# Add and Delete a Kyma Module

To use a Kyma module, you must add it first. Use Kyma dashboard or Kyma CLI to do that. If you don't need the module anymore, delete it to save resources.





## Add and Delete a Kyma Module Using Kyma Dashboard

Use Kyma dashboard to add and delete a Kyma module in the release channel of your choice.





## Context

If there are no modules added on your cluster, you can easily add one from the *Cluster Details* view. Select *Add Module* and follow the wizard steps.

If you want to add more modules, follow this procedure:





## Procedure

1.  Log in to Kyma dashboard. The URL is in the *Overview* section of your subaccount.

2.  In the *Kyma* section, choose *Modify*.

3.  Select *Edit*.

4.  In *Kyma Default Channel*, you can change the release channel for all your modules at the Kyma custom resource \(CR\) level, or keep the default one.

    > ### Note:  
    > By default, Kyma modules are part of the regular channel. It allows for delivering the modules at a slower, predictable rate for production environments with minimal disturbance. You can change to the fast channel that offers the latest technical updates and features at a quicker pace. For more information about the release channels, see [Kyma Release Channels](https://help.sap.com/docs/btp/sap-business-technology-platform/kyma-s-modular-approach?locale=en-US&version=Cloud#kyma-release-channels).

5.  In the *Modules* section, check the modules you want to add.

6.  **Optional:** At the module level, you can overwrite the release channel for the current module by choosing the available channel.

7.  Select *Update*.






## Results

This process may take a while, depending on the number of modules. The operation was successful when the module status changes to ***READY***.





## Next Steps

-   To configure your module, use the module CR that you can find in the module repository.

-   To delete a module, edit your Kyma instance, uncheck the modules you want to delete, and choose *Update*.






## Add and Delete a Kyma Module Using Kyma CLI

Use Kyma CLI to add or delete a Kyma module in the release channel of your choice.





## Context

To add a module using [Kyma CLI](https://github.com/kyma-project/cli), perform the following steps:





## Procedure

1.  Check which modules are available on your cluster. Run:

    ```
    kyma alpha list module
    ```

    You should get a result similar to this example:

    ```
    operator.kyma-project.io/module-name    Domain Name (FQDN)         Channel     Version     Template                                      State
            cluster-ip                   kyma-project.io/cluster-ip    fast       v0.0.24    kyma-system/moduletemplate-cluster-ip-fast   <no value>
    ```

2.  Add a module on your cluster in the release channel of your choice. Run:

    ```
    kyma alpha add module {MODULE_NAME} --channel {CHANNEL_NAME} --kyma-name default --wait
    ```

    You should see the following message:

    ```
    - Successfully connected to cluster
    - Modules patched!
    ```






## Next Steps

-   To configure your module, use the module CR that you can find in the module repository.

-   To delete a module, run:

    ```
    kyma alpha delete module {MODULE_NAME} --kyma-name default
    ```


**Related Information**  


[Kyma's Modular Approach](kyma-s-modular-approach-95a4101.md "With Kyma's modular approach, you can install only the modules you need, instead of a predefined set of components.")

[Kyma Release Channels](kyma-s-modular-approach-95a4101.md#loio95a410144d7c449687c957da0cc43a0d__section_kyma_release_channels)

[Kyma Modules](kyma-modules-0dda141.md "With Kyma's modular approach, you can install just the modules you need, instead of a predefined set of components.")

[https://github.com/kyma-project/cli](https://github.com/kyma-project/cli)

