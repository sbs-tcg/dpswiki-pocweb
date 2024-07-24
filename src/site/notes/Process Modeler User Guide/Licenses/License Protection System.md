---
{"dg-publish":true,"permalink":"/process-modeler-user-guide/licenses/license-protection-system/"}
---


The [[Primus\|Primus]] process management system and the [[Process Modeler\|Process Modeler]] are license protected. The license protection includes different licenses for the design-time, the runtime, and activities. 

---
## Demo licenses

After the initial Primus installation there is a free trial period that allows you to test the platform functionality. During the trial period, you can skip or postpone the platform activation and you can import and deploy a demo license to use the runtime. The demo license is available in the installation folder and allows processing up to 10.000 pages for a period of maximum 15 days after its registration. However, to run a process that performs full text recognition, classification, and extraction you require activity licenses for these activities. During the trial period you may either need specific activity licenses that work together with the demo license or you activate your platform and then import the activity licenses for the activated platform.

## Designtime license

The system comes with an installed designtime license that allows you to have one runtime environment, 10 processes, and 200 activities. If you plan to maintain several runtime environments from one design-time to deploy your processes to a testing, staging, and production system, you require a different design-time license. You can't set up and publish to a second environment until you register the appropriate designtime license.

## Runtime licenses

For runtime licenses, we distinguish between **platform** and **activity** licenses.

**Platform license** : Protects the platform itself to a certain functionality and volume.

**Activity license** : Protects an individual activity. It can protect a certain functionality, the so-called payload, and can [[Process Modeler User Guide/Licenses/Volume Counters\|count the volume]] for the processed documents, pages, or media. Whether an activity has a payload or volume counter depends on the activity.

>[!tip] Tip
>Refer to an individual activity's [[DocProStar Activity List\|Help Page]] for more information about what kind of activity license is required.

---

[[Process Modeler User Guide/Licenses/Platform Activation\|Platform Activation]] is carried out once. By default, the license activation file that you get for the platform activation is a license bundle that contains a platform and other required design-time and activity licenses. However, you can add other licenses at a later point of time as needed.

An administrator can activate the platform and [[License maintaining\|maintain the designtime, runtime, and activity license]]. 

As you can manage different runtime environments in [[Process Modeler\|Process Modeler]], the system stores licenses in the [[designtime database\|designtime database]] so that you can deploy them to any [[environment\|environment]].

## Requesting a license

License requests are used to **activate** the platform, to order **new licenses** or to order an **extension** for an existing license.

The license request file is a JSON file that contains the system identifiers the licensor requires to create valid licenses for this system. You can create the license request by clicking **DOWNLOAD LICENSE REQUEST**. Enter the information about the licenses you require. When you click **OK**, a JSON file with all needed information and a current license status is automatically downloaded. You then send the license request file to your license provider, , so that you get the requested runtime or OCR license in return.

>[!info] More information
>- [[Request a DocProStar license\|Request a DocProStar license]]
## Importing and deploying licenses

**Designtime licenses** : Are valid immediately after importing them. However, to protect a process with a password license, you have to assign the license to a process.

**Runtime licenses** : Are first imported into the license pool and need to be deployed to an environment to be used. An *imported* license has the "Activated" status whereas a *deployed* license ha the "Deployed" status.

For an environment, you can deploy one license for each [[Process Modeler User Guide/Licenses/License modes\|License modes]], one one-time and one renewable license. Refer to the [[Process Modeler User Guide/Licenses/License Consumption\|License Consumption]] topic for more information about how and which license counters are decreased when two licenses are deployed.

>[!info] More information
>- [[Process Modeler How-To/Deploy Platform or Activity Licenses\|Deploy Platform or Activity Licenses]]

## Modifying licenses

An already-deployed license can been retracted from one environment and deployed with its current license counters to another environment with the same type (-> [[Process Modeler User Guide/Licenses/License types\|License types]])

Licenses can also be [[Process Modeler How-To/Split Platform or Activity Licenses\|split]], [[Process Modeler How-To/Merge Platform or Activity Licenses\|merged]], [[Process Modeler How-To/Delete Platform or Activity Licenses\|deleted]], and [[Process Modeler How-To/Replace Platform or Activity Licenses\|replaced]] by other activated runtime licenses. Once again, both licenses worked on must have the same [[Process Modeler User Guide/Licenses/License modes\|License modes]].

When deleting a license, a JSON file is created. We recommend keeping this as proof that the license was deleted from the system. A deleted license cannot be re-imported : attempting to do so will return an error.

>[!example] Example
>- Split a license to use the newly created license for an additional runtime system.
>- Merge a license for an unused environment with one in use to assign the license volume to the used environment.
>- Replace a license with a new one when the former expires.

The above license management can be carried out by administrator users : non admins can only view the available licenses and refresh the current license counts.

## License Report

If you have licensed a subscription for the Primus platform, you are obliged to report the consumed volume to your licensor at regular intervals. The [[Process Monitor\|Process Monitor]] allows setting a billing period and creating a license report for the configured period within the **Licenses** mode.










