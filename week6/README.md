# Assignment for Week 6: Monitoring, Measurement, & Notification


### Alarm: CPU Utilization

	You are receiving this email because your Amazon CloudWatch Alarm "awsec2-i-0b41c232eabc69685-CPU-Utilization" in the US West (Oregon) region has entered the ALARM state, because "Threshold Crossed: 1 datapoint [2.88135593220462 (05/08/19 16:54:00)] was greater than or equal to the threshold (2.0)." at "Monday 05 August, 2019 17:04:03 UTC".

	View this alarm in the AWS Management Console:
	https://us-west-2.console.aws.amazon.com/cloudwatch/home?region=us-west-2#s=Alarms&alarm=awsec2-i-0b41c232eabc69685-CPU-Utilization

	Alarm Details:
	- Name:                       awsec2-i-0b41c232eabc69685-CPU-Utilization
	- Description:                Created from EC2 Console
	- State Change:               INSUFFICIENT_DATA -> ALARM
	- Reason for State Change:    Threshold Crossed: 1 datapoint [2.88135593220462 (05/08/19 16:54:00)] was greater than or equal to the threshold (2.0).
	- Timestamp:                  Monday 05 August, 2019 17:04:03 UTC
	- AWS Account:                006170570170

	Threshold:
	- The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 2.0 for 300 seconds. 

	Monitored Metric:
	- MetricNamespace:                     AWS/EC2
	- MetricName:                          CPUUtilization
	- Dimensions:                          [InstanceId = i-0b41c232eabc69685]
	- Period:                              300 seconds
	- Statistic:                           Maximum
	- Unit:                                not specified



	State Change Actions:
	- OK: 
	- ALARM: [arn:aws:sns:us-west-2:006170570170:defaultName]
	- INSUFFICIENT_DATA: 


### Alarm: Network Out

	You are receiving this email because your Amazon CloudWatch Alarm "awsec2-i-0b41c232eabc69685-High-Network-Out" in the US West (Oregon) region has entered the ALARM state, because "Threshold Crossed: 1 datapoint [385007.6 (05/08/19 18:12:00)] was greater than or equal to the threshold (100000.0)." at "Monday 05 August, 2019 18:17:25 UTC".

	View this alarm in the AWS Management Console:
	https://us-west-2.console.aws.amazon.com/cloudwatch/home?region=us-west-2#s=Alarms&alarm=awsec2-i-0b41c232eabc69685-High-Network-Out

	Alarm Details:
	- Name:                       awsec2-i-0b41c232eabc69685-High-Network-Out
	- Description:                Created from EC2 Console
	- State Change:               OK -> ALARM
	- Reason for State Change:    Threshold Crossed: 1 datapoint [385007.6 (05/08/19 18:12:00)] was greater than or equal to the threshold (100000.0).
	- Timestamp:                  Monday 05 August, 2019 18:17:25 UTC
	- AWS Account:                006170570170

	Threshold:
	- The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 100000.0 for 300 seconds. 

	Monitored Metric:
	- MetricNamespace:                     AWS/EC2
	- MetricName:                          NetworkOut
	- Dimensions:                          [InstanceId = i-0b41c232eabc69685]
	- Period:                              300 seconds
	- Statistic:                           Average
	- Unit:                                not specified



	State Change Actions:
	- OK: 
	- ALARM: [arn:aws:sns:us-west-2:006170570170:defaultName]
	- INSUFFICIENT_DATA: 


### Alarm: Network In

	You are receiving this email because your Amazon CloudWatch Alarm "Alarm: Network In" in the US West (Oregon) region has entered the ALARM state, because "Threshold Crossed: 1 datapoint [608545.6 (05/08/19 18:29:00)] was greater than or equal to the threshold (10000.0)." at "Monday 05 August, 2019 18:39:12 UTC".

	View this alarm in the AWS Management Console:
	https://us-west-2.console.aws.amazon.com/cloudwatch/home?region=us-west-2#s=Alarms&alarm=Alarm%3A%20Network%20In

	Alarm Details:
	- Name:                       Alarm: Network In
	- Description:                Created from EC2 Console
	- State Change:               OK -> ALARM
	- Reason for State Change:    Threshold Crossed: 1 datapoint [608545.6 (05/08/19 18:29:00)] was greater than or equal to the threshold (10000.0).
	- Timestamp:                  Monday 05 August, 2019 18:39:12 UTC
	- AWS Account:                006170570170

	Threshold:
	- The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 10000.0 for 300 seconds. 

	Monitored Metric:
	- MetricNamespace:                     AWS/EC2
	- MetricName:                          NetworkIn
	- Dimensions:                          [InstanceId = i-0452d48149a10f8f7]
	- Period:                              300 seconds
	- Statistic:                           Average
	- Unit:                                not specified



	State Change Actions:
	- OK: 
	- ALARM: [arn:aws:sns:us-west-2:006170570170:defaultName]
	- INSUFFICIENT_DATA: 

