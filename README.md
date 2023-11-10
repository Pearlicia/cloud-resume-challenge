# Create a CI/CD Pipeline with AWS CodePipeline & GitHub

Incorporate a CI/CD pipeline to automate the deployment of our Website whenever we make changes to the code.

We will be utilizing AWS CodePipeline, GitHub and Amazon S3! 

### Background
#### Continuous Integration (CI)
Continuous Integration is a practice that involves developers making small changes and checks to their code which helps streamline code changes. When practicing CI, new code changes to an app are regularly built, tested, and merged to a shared repository. It provides a solution to the problem of having too many branches of an app in development at once that might conflict with each other, thereby increasing time for developers to make changes and contribute to improved software.

#### Continuous Deployment/Delivery (CD)
Continuous Delivery is the automated delivery of completed code to environments for example, testing or development. CD provides an automated and consistent way for code to be delivered to these environments.

#### Continuous Deployment 
Is the next step of Continuous Delivery. Every change from a repository that passes the automated tests is automatically placed in production, where it is usable by customers. It improved the issues of overloading operations teams with manual processes that slow down app delivery to customers.

#### AWS CodePipeline (CodePipeline)
CodePipeline is a fully managed continuous delivery service on AWS that you can use to automate CI/CD pipelines for fast and reliable application and infrastructure updates.

#### GitHub
GitHub, as the name suggest, is a Hub, a central site that offers developers a cloud-based service to store and manage code as well as track and control changes to code. GitHub makes it possible to leverage Git in the cloud at a central site.

### Prerequisites
AWS account and IAM user
Website files (HTML, CSS)
GitHub Account

### Use Case
Whenever you want to update your Website to add new changes for everyone else to see. Currently when you make updates, you manually edit your Website files on your local system, delete the old file versions from S3, then upload the updated changes to the S3 bucket. You’ve now decided to move towards manually automate the deployment of the changes to the website by creating a CI/CD pipeline using AWS CodePipeline and GitHub and Amazon S3.

### Step 1: Create a new repository in GitHub and upload Website files.
Head to your GitHub account and create a new repository by clicking “New”.
![]()
Give the repository a name and description. Set it to “Public”, select “Add a README file”, then click “Create repository”.
![]()

Navigate to “Add file”, then upload your Website files.
![]()

After choosing your files, add a commit description, then click “Commit changes”.
![]()

You should now be able to see your files listed in your repository.
![]()

### Step 2: Connect GitHub Account to CodePipeline
Navigate to the CodePipeline service and Click on “Create pipeline”.
![]()

Name your pipeline and select “New service role”. Leave the rest of the settings at default, then click “Next”.
![]()

For the source stage, select “GitHub (Version 2)” as our source provider.

We can now connect our GitHub by selecting “Connect to GitHub”. Name the connection, then “Connect to GitHub”. You’ll need to sign in to your GitHub account to authorize the connection.
![]()

Click “Install new app”, select your Website repository, click “Install”, then click “Connect”.