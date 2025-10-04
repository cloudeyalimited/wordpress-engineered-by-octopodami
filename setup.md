# WordPress Engineered by OCTOPODAMI (WEBO) Setup

Our pre-configured stack relies on AWS EC2 which helps to improve performance and scalability of your WordPress site, but additional integration with other AWS services like S3, CloudFront, Route53, and Auto Scaling is possible.

## Preliminary Setup

You need to create a unique EC2 Key Pair so you can log into your EC2 instance easily. Within the AWS Management Console:

1. Go to **EC2** > **Network & Security** > **Key Pairs**
2. Click **Create Key Pair**
3. Enter a Key pair name and click **Create**
4. Download your Key pair with a **.pem** extension and store it in a safe place on your computer.

## Launch Instance

Within the EC2 Dashboard page, you can do the following to launch a WordPress Engineered by OCTOPODAMI (WEBO) instance:

1. Click the **Launch Instance** button or click this button [![Launch Stack](./images/launch-stack.png?raw=true)](https://go.aws/3I778nB)
2. Next, click **AWS Marketplace** tab on the left side of the **Choose an Amazon Machine Image (AMI)** page
3. Enter the phrase **octopodami** in the search box and press **enter** on your keyboard
4. Click the **select** button in front of WordPress Engineered by OCTOPODAMI®
5. Click the **continue** button in the dialog box
6. Select an instance type that fits your budget then click the **Review and Launch** button
7. Configure these options (**Security Groups**, **Instance Details**, **Storage**, and **Tags**) to match your business needs
8. Click the **launch** button

## Setup Your Site

Within the EC2 Dashboard page, click **Instance** to view your running instance, if any.

1. Select the instance you launched to view its detailed descriptions
2. Click the icon in front of **IPv4 Public IP** to copy the IP Address of the server to clipboard
3. Paste the IP Address in your browser (Chrome, Firefox, and IE. e.t.c.)
4. You will be presented with the screen below:

![Octopodami Instance ID|512x397, 20%](./images/octopodami_initial_screen.jpg?raw=true "Octopodami Instance ID")

5. Copy the **Instance ID** from your EC2 dashboard, paste it in the input field and click the **Next Step** button to proceed
6. Select your preferred language on the WordPress installation page
7. Configure site information (**site** **title**, **username**, **password**, **your e-mail**, and **search engine visibility**)
8. Click **Install WordPress** button to continue

## Visit Your WordPress Site

That’s all you have to do. You will now be able to preview your new WordPress web site at the IP Address of the server. The admin area can be accessed at **128.57.48.454/wp-admin/**

**Please Note**: the IP Address above is not a real one -- yours will be unique. :wink:

Use the credentials you provided earlier to access the WordPress admin console. You can now install plugins, themes and configure your site.

![Rejoice](https://media.giphy.com/media/26xBFFYvGNMfPo9QQ/giphy.gif?raw=true "Rejoice")

## Wanna Geek Out? SSH Into The Server

To SSH into your EC2 instance:

1. ```cd``` to the location of your .pem key
2. Run ```chmod 600 mykey.pem``` to lock down your SSH key
3. Run ```ssh -i /path/my-key-pair.pem ec2-user@<your ip address>```

[![asciicast](https://asciinema.org/a/461919.svg)](https://asciinema.org/a/461919)

4. Bam!!! Have fun. Don't break anything, but if you do. Support is available [here](mailto:tech@cloudeya.org).
5. To retrieve your WordPress credentials, run: ```sudo cat /root/.wordpress-credentials```

## Links

1. [Product Website](https://aws.amazon.com/marketplace/pp/prodview-iyn7nuvxxqcjg)
2. [EULA](./octopodamiEULA.txt)
3. [Knowledgebase](https://github.com/cloudeyalimited/wordpress-engineered-by-octopodami/-/wikis/home)
4. [Issue Tracking](https://github.com/cloudeyalimited/wordpress-engineered-by-octopodami/-/issues)
5. [Changelog](./changelog.md)

## Support

[Email](mailto:tech@cloudeya.org) support is available to Amazon Web Services Marketplace Customers. We do not offer refunds, but you may terminate your WordPress Engineered by OCTOPODAMI (WEBO) Stack at any time.

## License

The documentation is published under [BSD 3-Clause License](license.txt).

## Copyright

(c) 2020 - 2025 [Cloudeya Limited](https://cloudeya.org).