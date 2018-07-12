# AWS_CodeDeploy_Example
<br />
Please make sure that you add the following files to your project for this to work
<br />
&nbsp;&nbsp;&nbsp;&nbsp; appspec.yml
<br />
&nbsp;&nbsp;&nbsp;&nbsp; the entire scripts folder
<br />
<a href="https://www.youtube.com/watch?v=F6oLG-LyIhc&t=372s">Tutorial</a>
<br />
<br />
1. Create IAM Roles. Reffer IAM.txt file for role policies. 
<br />
CodeDeploy & CodeDeployEC2Service
<br />
2. Create EC2 instance with following categories
<br />
<br />
&nbsp;&nbsp;&nbsp;&nbsp;    a. Choose AMI: Amazon Linux AMI
    <br />
    <br />
&nbsp;&nbsp;&nbsp;&nbsp;    b. Choose Instance type: t2.micro
    <br />
    <br />
 &nbsp;&nbsp;&nbsp;&nbsp;   c. Configure Instance: Choose CodeDeployEC2Service IAM role
    <br />
    <br />
  &nbsp;&nbsp;&nbsp;&nbsp;  d. Tag Instance: Name it what you please
    <br />
    <br />
  &nbsp;&nbsp;&nbsp;&nbsp;  e. Configure Security Group: 
    <br />
    <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        HTTP TCP 80 0.0.0.0/0
        <br />
        <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      HTTP TCP 80 ::/0
        <br />
        <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      SSH TCP 22 (YOUR IP ADDRESS)
        <br />
        <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      HTTPS TCP 443 0.0.0.0/0
        <br />
        <br />
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     HTTPS TCP 443 ::/0
        <br />
        <br />
&nbsp;&nbsp;&nbsp;&nbsp;    f. LAUNCH INSTANCE
    <br />
    <br />
3. Login to EC2 instance
<br />
<br />
4. Command line of Amazon Linux AMI 
<br />
<br />
&nbsp;&nbsp;&nbsp;&nbsp;    a. Copy codedeploy_Initial.sh and Execute it
    <br />
    <br />
 
  &nbsp;&nbsp;&nbsp;&nbsp;  b. Restart service and Verify it is running .
    <br />
    <br />
   &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;   service codedeploy-agent restart and service codedeploy-agent status

   
