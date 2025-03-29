
# Remote Teams
*Setup Instructions for remote teams:*

## General instructions 

Please put a video on display of your overall setup and a view of your power monitor. You will be trusted that you will not be accessing your cluster remotely, but leave the cameras on if you can.

For the Aalborg team: Please follow these times as close as possible in your respective time zone. You will be receiving the information on the mystery app as well.

For KU, Clemson, and TTU: Expectation is that you will be on call and aligning your hours to the ones here on the West Coast, PDT. If this is an issue, let us know.

## Application Announcements
For announcement of application specifications according to the [calendar](./sched.md) based on your local time zone. Please coordinate with Competition organizers.

## Networking
The main network constraint is having one exit point to the internet. And that the internet is unable to initiate connections into any of your servers. A computer that is solely running DHCP (or some sort of networking that solely assigns ips) can be excluded from your power budget. 

A central switch that has a DHCP for example, would count, but a router running DHCP connected to a central switch wouldn't.

## Power
For power, since you are remote, we expect you to have a log (aka your video stream recording) of your power and during submissions include a full log of your cluster's power consumption throughout the competition.

## Logs
Compress the paths where logs are often stored, usually just `/var`, from the head/login/main compute nodes. If your team believes that the logs after a certain number of nodes is too similar, exclude them. This means if you feel that node 1, node 2, node 3 have the most distinct logs, but the following nodes 4---12 nodes are just a repetition of the first 3 logs, just exclude them. We will ask for these files to be submitted at the end of the competition.

## Access
We're running on an honor code for remote teams to comply of not having access to their clusters after 5:00pm their time in fairness for the on-site teams.
