# IRI on AWS
A beginner guide to running an IOTA Headless Node on the Amazon Web Services Free Tier (https://aws.amazon.com/free/)

## Part 1: Setting up the instance
1) Create an account on http://aws.amazon.com
2) Navigate to the EC2 dashboard https://console.aws.amazon.com/ec2
3) Ensure that your region is US East (N. Virginia) in the upper right corner (more regions coming soon)
4) In the left sidebar, click "Instances", and then "Launch Instance"
5) On the left, click "Community AMIs" and search for ami-7c5e0c6a
6) Click Select, and then click your desired configuration. Note that only t2.micro is eligible for the free tier.
7) Click "Next: Configure Instance Details"
8) Optional: Check off "Protect against accidental termination". This will prevent you from accidentally deleting your node. 
9) Click "Next: Add Storage". You don't need to change any of these unless you anticipate needing more than 8GiB (8.5GB) of storage.
10) Click "Next: Add Tags" and then "Next: Add Security Groups"
11) Ensure that you are creating a new security group. You can name it whatever you want or leave it as the default. A security group is essentially port forwarding rules. You will need to set this up later in order to access your node from the internet.
12) Click "Review and Launch"
13) You will now be asked to provide a key pair. This ensures that only you can access the command line of your node. Select "Create a new key pair" and then "Download Key Pair". Make sure you save the key pair somewhere safe, as the node will be inaccessbile if you lose it.
14) Launch the instance, and then at the top click Services>EC2 to go back to the dashboard
15) Click "Instances" in the left sidebar. Your instance will start up. In the mean time, you should set up some other things for your node.

## Part 2: Instance options
1) In the left sidebar, select "Security Groups"
2) Select the security group that is linked to your instance
3) Go to Actions>Edit inbound rules and enter the rules as shown in the screenshots. Then follow the screenshot for the outbound rules.
