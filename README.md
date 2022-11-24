# Setting up your environment

Before starting the exercises, you'll need to get set up with a SageMaker notebook environment and clone in the [workshop code repository](https://github.com/MichaelDasseville/Autogluon-Workshop.git).

::::::tabs{variant="container" groupId=EventType}
:::::tab{label="AWS Hosted Event"}

::alert[Only follow the instructions on this tab if you are at an AWS-hosted event with temporary accounts provided. If running on your own account, see the 'Your own AWS Account' tab instead.]{type=warning}

::alert[Note that temporary accounts will be terminated after the end of the event. If you want to save any work you've done here, please download it to your local desktop as we wrap up the event.]{type=info}


#### Log in to the AWS workshop portal

In workshop-provided accounts, the SageMaker environment should be set up for you automatically. You will need the **Hash Code** provided upon entry, and your email address to track your unique session.

Connect to the portal by clicking the link or browsing to [https://dashboard.eventengine.run/](https://dashboard.eventengine.run/).

![](/static/images/setup/EventEngine-Home.png "Screenshot of Event Engine login page")

Enter the provided hash in the text box. The button on the bottom right corner changes to **Accept Terms & Login**. Click on that button to continue.

You'll be asked to verify your identity either via an **Email One-Time Password** or logging in with your **Amazon.com retail account**.

![](/static/images/setup/EventEngine-Verify-Methods.png "Event Engine identity verification prompt")

:::alert{type=info}
You can choose whichever method is most convenient for you... But if using Email OTP, be sure to enter an email address you have access to so you can retrieve the code.
<br/><br/>
Email OTPs may take a few minutes to come through, so please be patient and remember to check your junk folder!
:::

Once verification is complete, you'll be directed to your *team dashboard* as shown below:

![](/static/images/setup/EventEngine-Team-Dashboard.png "Event Engine team dashboard after login")


#### Open the AWS Console and Amazon SageMaker

From your Event Engine team dashboard, click **AWS Console**. This will open the AWS Console Login dialog (shown below), from which you can open your temporary account's AWS console or even copy CLI credentials for the account.

::alert[If you're currently logged in to a different AWS Account, you'll need to log out of that one first. Alternatively, you could access both at the same time by clicking **Copy Login Link** and opening the temporary account in a private or sandboxed browsing window]{type=warning}

![](/static/images/setup/EventEngine-Console-Login.png "Event Engine AWS Login dialog")

After opening the AWS Console, **check** with the instructors that you're working in the correct AWS Region for this event and switch regions if necessary, using the drop-down in the top right corner (highlighted in the screenshot below).

Then, use the search bar in the top of the console to open the [Amazon SageMaker Console](https://console.aws.amazon.com/sagemaker/).

![](/static/images/setup/AWS-Open-SageMaker.png "Check region and open SageMaker from the AWS Console home page")


#### Open SageMaker Studio

Amazon SageMaker Studio should already have been provisioned for you in the temporary account.

- From the SageMaker Console, click **Amazon SageMaker Studio** in the left sidebar menu
- You'll see a list of usernames with a user already created for you
- Click **Open Studio** next to your username to open SageMaker Studio

A new tab will open to the SageMaker Studio UI for your user, as shown below.

![](/static/images/studio-new-ui.png)

::alert[If you see a loading screen when opening Studio for the first time, don't worry: This initial process can sometimes take a few minutes to complete. If it's been longer than ~5 minutes, try refreshing the tab or closing it and clicking **Open Studio** again.]{type=info}

#### Check your setup

In Studio, you should see that the `sagemaker-101-workshop` code has already been downloaded for you (in the folder tab on the left hand side). If not, you can ask our instructors for help or switch this walkhrough page to the "Your own AWS Account" tab and try following the "Fetch the workshop code" guidance to download it yourself.

:::::
:::::tab{id="angular" label="Your own AWS Account"}

::alert[Only follow the instructions in this section if you are running on your own account and not during an AWS-hosted event.]{type=warning}

The labs in this workshop assume you have:

- A SageMaker notebook environment set up, with
- Outbound internet access, and
- The workshop code loaded onto the notebook, and
- An attached *Execution Role* with sufficient permissions to access the default SageMaker bucket in your account/region, and perform basic SageMaker tasks like running training jobs and deploying endpoints.

The preferred notebook environment for completing the exercises is **SageMaker Studio**.

- You can find detailed guidance on how to set up SageMaker Studio [here in the SageMaker Developer Guide](https://docs.aws.amazon.com/sagemaker/latest/dg/gs-studio-onboard.html).
- For simple initial testing, you may find it easiest to [onboard with IAM](https://docs.aws.amazon.com/sagemaker/latest/dg/onboard-iam.html). Configuring a SageMaker Studio domain involves a few high-level design decisions, but you can always delete your test domain and create a new one later if you need to.

![](/static/images/setup/Domain-Users-Custom.png "Screenshot of SageMaker Studio Console listing users")

**If you're not able** to use Studio, you can instead set up a [SageMaker Notebook Instance](https://docs.aws.amazon.com/sagemaker/latest/dg/gs-setup-working-env.html). We'd recommend an instance type of `ml.t3.medium`. Once your notebook instance is created, you can click **Open JupyterLab** for a roughly similar user experience to SageMaker Studio.

![](/static/images/setup/NBI-List-Custom.png "Screenshot of SageMaker Console listing notebook instances")


#### Fetch the workshop code

Once you've created your notebook environment, open it by clicking either **Open Studio** (for SageMaker Studio) or **Open JupyterLab** (for Notebook Instance).

To fetch the workshop code, first open a **System Terminal** (Studio has two terminal options: System and Image)

![](/static/images/setup/Studio-Launcher-SystemTerm-Highlight.png "SageMaker Studio launcher screen with system terminal highlighted")

::::alert{header="If you're running in a notebook instance" type=warning}
In a notebook instance, you'll have to run the following command first to move to the Jupyter root folder (the one visible in the folder tree in the left sidebar):

:::code{showCopyAction=true}
cd ~/SageMaker
:::

::::

Then, run the command below to clone the repository:

:::code{showCopyAction=true}
git clone https://github.com/MichaelDasseville/Autogluon-Workshop.git
:::

Once done, you should see the workshop code in the folder sidebar UI as shown below.

![](/static/images/setup/Studio-Git-Clone-Workshop.png)

Congratulations, you're now ready to tackle the labs!
:::::
::::::

