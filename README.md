# Open Source Monitoring application

![image](monitoring.png)

<h2> CI/CD Pipeline for Uptime Kuma</h2>
<p>Uptime-Kuma is an open-source self-hosted monitoring tool that provides a sleek 
  interface to track the uptime of websites, services, and APIs. When integrated into 
  a CI/CD pipeline for a blog, it helps ensure continuous availability and performance 
  monitoring. Here’s a detailed explanation of how Uptime-Kuma can be utilized effectively in this context:</p>

<h3>What is Uptime Kuma</h3>
<div>
  <ul>
    Overview: Uptime-Kuma is a self-hosted monitoring tool designed to track
    the uptime and performance of websites, services, and APIs.
  </ul>
  <h4>Features</h4>
  <ul>
    <li>Real-time monitoring with customizable intervals</li>
    <li>Alerts via multiple channels (email, slack, Telegram,etc</li>
    <li>Historical data and uptime statistics</li>
    <li>Sleek, User-friendly interface</li>
  </ul>
</div>
 <b> Now, let's get started anddig deeper into each of these steps:</b>
<h1>1. AWS Account and login</h1>
<ul>
  <li>If you don't have and AWS account sign up at <a href="https://aws.amazon.com/activate/registration">AWS Sign Up</li>
  <li>Login to AWS management Console.</li>
</ul>

 <h2><strong>A.Navigate to Ec2 Dashboard</strong></h2>
<h3>2. Launch an Ec2 instance</h3>
<ul>
  <li>Go to the <a href="https://aws.amazon.com/console/ec2/">EC2 Dashboard</a>
</li>
</ul>
<h2>B.Choose an Amazon Machine Image (AMI):</h2>
<ul>
  <li>click "Launch Instance"</li>
  <li>In the AMI Selection Screen for "Ubuntu 24.04".</li>
</ul>
<h2>C. Choose an Instance Type:</h2>
<ul>
  <li>select t2.large instance</li>
  <li>Click "Next: configure instance Details</li>
<h2>D. Configure Instance Details</h2>
  <ul>
    <li>Use the default settings</li>
    <li>Ensure you have selected the correct VPC and subnet</li>
    <li>Click "Next: Add Storage</li>
  </ul>
<h2>E.Add Storage</h2>
<ul>
  <li>Modify the root volume size to 30GB</li>
  <li>Click "Next: Add Tags"</li>
</ul>
<h2>F.Next Add Tags</h2>
<ul>
  <li>(optional) Add tags for better management</li>
  <li>Click "Next: Configure Security Group"</li>
</ul>
<h2>G. Configure Security Groups</h2>
  <ul>
    <li>create a new security group</li>
    <li>Set the security group name and description</li>
    <li>Add a rule to allow all traffic(not recommended for production environments)</li>
    <ul>
      <li>Type:All Traffic</li>
      <li>Protocol:All</li>
      <li>Port Range:All</li>
      <li>Port Range:22, 80,443,8080,9000,3001,5000,</li>
      <li>Source:0.0.0.0/0(for Ipv4) and ::/0(for Ipv6)</li>
    </ul>
  </ul>
</ul>
