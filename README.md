# Setting up Your Environment

Follow these instructions to get set up with a SageMaker notebook environment and to clone the [workshop code repository](https://github.com/MichaelDasseville/Autogluon-Workshop.git).

> **Note**
> Only follow the instructions on this tab if you are at an AWS-hosted event with temporary accounts provided.

> **Note**
> Temporary accounts will be terminated after the end of the event. If you want to save any work you've done here, please download it to your local computer.

## Log in to the AWS Workshop Portal

In an AWS-hosted event, the SageMaker environment is set up for you automatically.
You will need the **Hash Code** provided upon entry, and your email address to track your unique session.

Connect to the portal by clicking the link or browsing to **[https://dashboard.eventengine.run/](https://dashboard.eventengine.run/)**.

![](/static/images/setup/EventEngine-Home.png "Screenshot of Event Engine login page")

Enter the provided hash in the text box. The button on the bottom right corner changes to **Accept Terms & Login**. Click on that button to continue.

You'll be asked to verify your identity either via an **Email One-Time Password** or logging in with your **Amazon.com retail account**.

![](/static/images/setup/EventEngine-Verify-Methods.png "Event Engine identity verification prompt")

> **Note**
> When using Email OTP, be sure to enter an email address you have access to so you can retrieve the code.
<br/><br/>
Email OTPs may take a few minutes to come through, so please be patient and remember to check your junk folder!

Once verification is complete, you'll be directed to your *team dashboard*:

![](/static/images/setup/EventEngine-Team-Dashboard.png "Event Engine team dashboard after login")


## Open the AWS Console

You are redirected to the Team Dashboard. Click on AWS Console.

![](/static/images/setup/EventEngine-Console-Login.png "Event Engine AWS Login dialog")

On the next screen, click on **Open AWS Console**.

![](/static/images/setup/open-console-2.png "Event Engine AWS Login dialog")

After opening the AWS Console, please do not change the AWS Region for this event.

## Navigate to Amazon SageMaker

Use the search bar in the top of the console to open the [Amazon SageMaker Console](https://console.aws.amazon.com/sagemaker/).

![](/static/images/setup/AWS-Open-SageMaker.png "Check region and open SageMaker from the AWS Console home page")

#### Open SageMaker Studio

Amazon SageMaker Studio should already have been provisioned for you.

- From the SageMaker Console, click **Amazon SageMaker Studio** in the left sidebar menu
- You'll see a list of usernames with a user already created for you
- Click **Open Studio** next to your username to open SageMaker Studio

A new tab will open to the SageMaker Studio UI for your user, as shown below.

![](/static/images/setup/Studio-Launcher-SystemTerm-Highlight.png "SageMaker Studio launcher screen with system terminal highlighted")

> **Note**
> If you see a loading screen when opening Studio for the first time, don't worry: This initial process can sometimes take a few minutes to complete. If it's been longer than ~5 minutes, try refreshing the tab or closing it and clicking **Open Studio** again.

#### Fetch the Workshop Code

In the SageMaker notebook, click on the **Launch Terminal in current SageMaker Image** icon. The kernel must be fully started (the circle on the right next to the Share button must be empty) to be able to click on the icon.

![](/static/images/setup/terminal-button.png "Terminal Button")

In the terminal, type the following command:

:::code{showCopyAction=true}
git clone https://github.com/MichaelDasseville/Autogluon-Workshop.git
:::

Once done, you should see the workshop code in the folder sidebar UI as shown below.

![](/static/images/setup/Studio-Git-Clone-Workshop.png)

**Congratulations!!** You are now ready to tackle the labs!
