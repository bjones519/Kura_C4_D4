## Purpose
Deploy a web application onto an EC2 instance using Jenkins and setup monitoring of the application using AWS CloudWatch

## Issues

## Steps
1. Create an instance with Jenkins "python3.10-venv", "python3-pip" and "ngnix" installed onto it
2. Run the Jenkins Pipeline
![pipeline](screenshots/Jenkins.png)

3. Navigate to the web application to make sure it was deployed correctly
![app](screenshots/URLShortner.png)

4. Install a cloudwatch agent onto the server using the [AWS Documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-commandline-fleet.html)

5. Navigate to metrics section in Cloudwatch on the AWS Console and you should see metrics labeles "CWAgent"

6. Since I wanted to se how the server was performing I selected the "cpu_usage_system" metric
![monitor](screenshots/CloudWatchD4.png)
 When I ran a second build the cpu spiked but not nearly as high as the first time.
![monitor2](screenshots/CloudWatch.2.png)


## Systems Diagram
![Design]()

## Optimization