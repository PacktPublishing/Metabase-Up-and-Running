# Chapter 2: Deploying Metabase with AWS Addendum

## Why this addendum

There is a known bug in AWS as of the publication of the book that may affect your ability to properly deploy Metabase using the link at https://www.metabase.com/docs/latest/operations-guide/running-metabase-on-elastic-beanstalk.html.

This bug prevents you from being able to edit the **Database** card in the environment configuration. The following is a workaround. There are two seperate areas in Chapter 2 where we learn how deploy Metabase using Elastic Beanstalk:


* Quick launch on Elastic Beanstalk
* Creating the Metabase application

Depending on which section you want to complete, you can find the paved path below:

## Quick launch on Elastic Beanstalk

If you encounter the bug, do the following:

1. Starting in AWS, select the Elastic Beanstalk service.
2. Click **Create Environment**
3. Keep the **Web server environment** radio button on and click **Select**.

On the next page, in the **Create a web app** section, fill out the following:

1. **Application information**: `Metabase`
2. **Environment information**: `Metabase-env` or anything you like.
3. **Domain**: If you want a specific domain name, add it here knowing it will be concatenated with `.us-east-1.elasticbeanstalk.com`.

In the **Platform** section:
1. **Platform**: `Docker`
2. **Platform Branch**: `Docker running on 64bit Amazon Linux 2`
3. **Platform version**: `3.1.2` or whatever is recommended.

In the **Application code** section, click the radio button to **Upload your code**.

Now, in the **Source code origin** section:

1. In the version label section, type `metabase-ebs`

We will be uploading a **Local File**, so first [visit this URL and download the file.](https://github.com/PacktPublishing/Metabase-Up-and-Running/chapter2/Dockerrun.aws.json)

2. Keeping the **Local File** radio button on, click the **Choose file** button and select the `Dockerrun.aws.json` file you just downloaded.
3. Click the **Configure more options** button.

This will take you to the configuration page. You can now follow along with the book at the **Configuring your application for quick launch** section. The only thing to note is that **you must fill out the Database card before filling out the Network card**.


## Creating the Metabase application

If you are following the "Best Practices" guide and encounter the bug, here's what do do:

1. Starting in AWS, select the Elastic Beanstalk service.
2. Click **Create Environment**
3. Keep the **Web server environment** radio button on and click **Select**.

On the next page, in the **Create a web app** section, fill out the following:

1. **Application information**: `Metabase`
2. **Environment information**: `Metabase-env` or anything you like.
3. **Domain**: If you want a specific domain name, add it here knowing it will be concatenated with `.us-east-1.elasticbeanstalk.com`.

In the **Platform** section:

1. **Platform**: `Docker`
2. **Platform Branch**: `Docker running on 64bit Amazon Linux 2`
3. **Platform version**: `3.1.2` or whatever is recommended.

In the **Application code** section, click the radio button to **Upload your code**.

Now, in the **Source code origin** section:

1. In the version label section, type `metabase-ebs`

We will be uploading a **Local File**, so first [visit this URL and download the file.](https://github.com/PacktPublishing/Metabase-Up-and-Running/chapter2/Dockerrun.aws.json)

2. Keeping the **Local File** radio button on, click the **Choose file** button and select the `Dockerrun.aws.json` file you just downloaded.
3. Click the **Configure more options** button.

This will take you to the configuration page:

On the **Configure Metabase-env** page, under **Presets**, click the **Custom configuration** radio button.

The only differences in filling out the configuration from the print version are:

### Capacity

The `t2.micro` instance type will be the default selection. This is the type to use if you want to remain on the free tier, otherwise I recommend using `t2.small`.

### Database

It's important to fill this out **before you fill out the Network section**. Otherwise you will not see the **Database settings** section in the Network configuration. 

### Network

As mentioned above, make sure to fill this section out **after** you fill out the Database section. 

Otherwise, it follows the same as in the book. Once you're done, click **Create app**