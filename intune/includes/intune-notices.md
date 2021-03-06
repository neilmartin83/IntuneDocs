
These notices provide important information that can help you prepare for future Intune changes and features. 

### Change in enrollment workflow with Intune Company Portal on corporate iOS devices authenticating with Setup Assistant <!-- 1927359 -->
There's an upcoming change in workflow for enrollment of iOS devices through one of Apple’s corporate device enrollment methods - Apple Configurator, Apple Business Manager, Apple School Manager, or the Apple Device Enrollment Program (DEP), when using Setup Assistant for authentication. This change applies only to devices enrolled with user affinity.

#### How does this affect me?
When this change is rolled out in ~~March~~ April, enrollment profiles in Intune in the Azure portal will be updated so that you can specify how devices authenticate and if they receive the Company Portal app. There will be an improved workflow to enroll iOS devices through the methods listed above. Note:

- When enrolling new devices and authenticating with Setup Assistant, you’ll be able to choose whether or not to deploy the Company Portal app automatically. End users will no longer see the “Identify your device” screen and the “Confirm your device” screen in the enrollment flow.  
- On devices already enrolled via Setup Assistant through one of Apple’s corporate device enrollment methods, you must take action if you want to enable Conditional Access. You’ll have to configure an app configuration policy with a specific xml to push the Company Portal down to these devices. Directions to do this are in the blog post at the Additional Information link. If you choose to push the Company Portal in this manner, end users will no longer see the “Identify your device” screen and the “Confirm your device” screen in the enrollment flow. 
- After this change is rolled out, if you haven't deployed the Company Portal with the app configuration profile mentioned above and if end users download the Company Portal app from the App store, they'll can sign in, but they'll get an error message. They won't be able to use the app for Conditional Access. 

#### What do I need to do to prepare for this change?
If you plan on using the modified workflow, you'll want to update your end user guidance to indicate that:

- End users will no longer see the two screens mentioned above in the enrollment flow. 
- They'll need to sign in to the Company Portal when it's automatically deployed and not download it from the app store. 

You can choose to create an app configuration policy now if needed, in preparation for this change. When this new workflow rolls out, you’ll see updated enrollment profiles in the console. We’ll also inform you of this rollout through the Message Center. After this, you’ll need to take the action so your end users can enroll through DEP by authenticating with Setup Assistant and you can use Company Portal for Conditional Access.

See our support blog post at the Additional Information link for more details about this change.

#### Additional Information 
[https://aka.ms/enrollment_setup_assistant](https://aka.ms/enrollment_setup_assistant)


### Company portal changes for iOS 12.2 enrollment in Intune
We shared in MC172534 that Apple has announced some changes related to iOS devices enrolling into Mobile Device Management (MDM) services. The change will likely be seen in the release of iOS coming up in March 2019 as well as all future iOS releases. We’re making some updates in the Company Portal to reflect Apple’s changes. 
 
#### How does this affect me?
If your end users upgrade their devices to iOS 12.2 and above, know that there's a modified workflow and they must take additional steps to complete enrollment into Intune. After the March update to Intune, here's what they'll do -  

- Begin the enrollment process in the Company Portal app to download a management profile
- Go to Settings > General > Profiles and look for a red badge notification
- Select the correct profile and click through to Install
- Return to the Company Portal to complete enrollment

Click Additional Information for detailed information on the enrollment flow.

Unless they're unenrolled and need a fresh enrollment, devices that are already enrolled and upgrade to iOS 12.2 and above shouldn't be affected. Enrollment experience on devices running iOS 12.1 or earlier won't change with this new release by Apple. Devices enrolled through one or Apple’s corporate enrollment methods (Device Enrollment Program, Apple School Manager or Apple Business Manager) won't be affected.

#### What can I do to prepare for this change?
You should plan to upgrade your documentation and your end user guidance. You may also want to let your helpdesk know of these changes. We’ll keep you informed through our What’s New page when this change goes live. 

If you want to take advantage of the Company Portal changes we’re introducing, ask your end users to update their device to the new iOS version after the March update to the Intune service when Company Portal app version 3.9.0. is released.

Click Additional Information for a support blog post with preview screenshots of the Company Portal changes.

Additional Information 
[https://aka.ms/CP_changes_iOS12](https://aka.ms/CP_changes_iOS12)

### Plan for Change: Workflow changes for iOS 12 enrollment in Intune
Apple has announced some changes related to iOS devices enrolling into Mobile Device Management (MDM) services. The change will likely be seen in the spring 2019 release of iOS as well as all future iOS releases.

#### How does this affect me?
If your end users upgrade their devices to this new version of iOS 12 in the spring, know that there's a modified workflow and they'll need to take additional steps to complete enrollment into Intune. When Apple introduces these changes, end users will have to:

- Begin the enrollment process in the Company Portal app to download a management profile
- Go to Settings > General > Profiles
- Select the correct profile and click through to Install
- Return to the Company Portal to complete enrollment 

Unless they're unenrolled and need a fresh enrollment, devices that are already enrolled and upgrade to the new iOS release shouldn't be affected.

Enrollment experience on devices running iOS 12.1 or earlier won't change with this new release by Apple.

#### What can I do to prepare for this change?
You should plan to upgrade your documentation and your end user guidance. You may also want to let your helpdesk know of these changes. We’ll keep you informed through the Message Center and our What’s New page when this change goes live.

#### Additional Information
[Support blog post with screenshots and video of the expected enrollment flow](https://aka.ms/iOS_enrollment_changes).

### Plan for Change: User experience update to Intune Company Portal app for iOS
We’re excited to share that Intune will soon be releasing a major user experience update to the iOS Company Portal app. The update will feature a visual redesign of the home page with advanced filters and faster access to apps and books.

#### How does this affect me?
This user experience update, while maintaining current iOS Company Portal functionality, will feature:
- A home page with native iOS look and feel 
- Filtering capabilities on content lists and search, including the ability to filter by content type (apps or ebooks) and availability (device management required or available without enrollment)
- Ability to search ebooks
- Search history for apps and ebooks

If you’re part of the Apple TestFlight program, you will be notified about the pre-release version of Intune’s updated iOS Company Portal app when it becomes available. If you’re not part of the Apple TestFlight program, it’s not too late to register. Registering will enable you to use the updated Company Portal app before it’s available to your end users. You'll can also provide feedback directly to the Intune team.  

#### What can I do to prepare for this change?
You don't need to take any action; these changes will be released in an upcoming iOS CP app release. 

#### Additional Information
[https://aka.ms/cp_update_iOS](https://aka.ms/cp_update_iOS)


### Reminder: Removal of existing Exchange Online to Intune connectors <!-- 3105122 -->
In MC165575, we shared that we would be removing the Exchange Online to Intune ‘Service to Service’ connector functionality in an upcoming update. With the February update to the Intune service, we’ll disable the button to set up new connectors. We are planning to remove all existing Exchange Online to Intune connectors in March 2019.
 
#### How does this affect me?
You are receiving this message since our records indicate that you may be using the ‘Service to Service’ connector functionality in your environment. 
The ‘Service to Service’ connector supports Intune management of Exchange Active Sync Only devices for Exchange Online and doesn't support on-premises infrastructure. This connector, because of the way it displayed in the console, appears to be necessary for Conditional Access (CA), when in reality, it's not needed for CA. You may have been using this connector to understand the usage of Exchange Online before applying Conditional Access. This information is already provided by the Microsoft 365 Admin Center. Here, you’ll find provides usage reports for Exchange Online including the app type being used for between 7 and 180 days. For more information see [Office 365 Reports in the Admin Center - Email apps usage](https://docs.microsoft.com/office365/admin/activity-reports/email-apps-usage?view=o365-worldwide).  
 
If you use this connector in your environment, you won’t be able to monitor or wipe Exchange Active Sync Only devices in Intune after connectors have been disabled in February. There's no anticipated impact to your end users during this change.
 
#### What can I do to prepare for this change?
If you have the Service to Service connector set up and have Exchange Active Sync Only devices, switch to other methods of managing your devices. You have the following options:

- Enroll devices in Mobile Device Management (MDM) 
- Use Intune App Protection Policies to manage your devices 
- Use Exchange controls as outlined in documentation [here](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/clients-and-mobile-in-exchange-online) 

#### Additional Information  
https://docs.microsoft.com/intune/exchange-service-connector-configure




### Check your “Delay Visibility of Software updates” setting in Intune 

We shared in MC171466 that we were moving a few settings around in the console. With the March update to Intune, we'll completely remove the “Delay Visibility of Software updates” setting from the iOS update policy blade. This will not change the way your scheduled software updates apply but it may affect how long the visibility of an update is delayed for end users. You may need to take action before the end of March if you use this setting. 

#### How does this affect me?
After the February Intune service update, you’ll notice that the setting appears both in Device restriction profiles in the console and in iOS update policies in the Software update blade. When you see this change reflected in the console, here’s what you may need to do.

- For existing Update policies for iOS: If you have custom configured this setting to anything other than the default 30 days, and want your existing configurations for the Delay visibility setting to continue to apply after the end of March, you’ll have to create a new iOS device restriction profile. Here, the Delay visibility setting will need to have the same values as in the existing iOS update policy and be targeted to the same groups. After the March service update, you will no longer be able to edit values for this setting in existing iOS update policies since it will no longer be visible in this blade. You will configure this setting in the new profiles instead.
  If the value for number of days you can delay visibility does not match in both locations for custom configured setting values, the Delay Visibility setting will not work, and end users will see the update on their devices as soon as it is available. This may have minimal impact for most customers since the other settings in the Software Update Policy blade have always taken precedence over this setting in the console.
- For new update policies for iOS: If you try to create new policies in the Software updates blade after the Intune February service update, you will see this setting grayed out. You’ll see a note in the console redirecting you to the Device configuration blade if you wish to delay visibility of updates.

#### What can I do to prepare for this change?
You do not need to take action if you do not use this setting or do not want to delay visibility of software updates for your end users.

If you wish to delay visibility of updates, start configuring the setting in new profiles in the Device Configuration blade under Device Restrictions > General. If you have this setting custom configured in existing iOS update policies, create a new equivalent device restriction profile with the same value for “days” to delay visibility of updates to your users, after the February update and before the March update rolls out. 

You may want to update your IT Pro guidance and inform your helpdesk.

See our support blog post at Additional Information for details on how to configure this setting.

#### Additional Information 
[https://aka.ms/Delay_visibility_setting_iOS](https://aka.ms/Delay_visibility_setting_iOS)
