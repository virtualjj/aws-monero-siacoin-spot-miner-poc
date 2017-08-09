# AUTOMATED SPOT INSTANCE SIACOIN AND MONERO MINING

- [PURPOSE](#purpose)
- [DISCLAIMER](#disclaimer)
- [STACK DEPLOYMENT](#stack-deployment)
- [RESULTS](#results)

# PURPOSE

This purpose of this project was to see how much hashing performance per spot instance price I could get mining [Siacoin](http://sia.tech/) and [Monero](https://getmonero.org/) cryptocurrencies on AWS g2 and p2 GPU instances.

# DISCLAIMER

Mining on AWS is not profitable and probably frowned upon by AWS. Although there is no specific mention in the [AWS Acceptable Use Policy](https://aws.amazon.com/aup/) about mining, AWS is multi-tenant and this type of activity is "noisy" and probably not the best use of AWS resources. In other words, have fun testing but don't run this everyday for 24 hours a day because it will be expensive and AWS might disable your AWS account.

# STACK DEPLOYMENT

[![Launch CloudFormation Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png
)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=siacoin-monero-miner&templateURL=https://s3-us-west-2.amazonaws.com/github-aws-monero-siacoin-spot-miner-poc/aws-monero-siacoin-spot-miner-poc.yml)

# RESULTS

You can read the details and play-by-play at my post [here](https://virtualjj.com/post/aws-sia-and-monero-mining-poc/) however, the most I observed for the Siacoin miner was between 434 ~ 458 MH/s and 93 H/s for the Monero miner on one p2.xlarge instance.

I did try launching 20 instances (max per region) concurrently in Ireland, N. Virginia, and Ohio. However, due to spot availability, only 12 launched in Ireland, 20 in N. Virginia, and 16 in Ohio for a total of 48 spot p2.xlarge instances. The ***peak*** aggregate hashing power I observed for Siacoin was 22.9 GH/s and about 6.2 KH/s for Monero.
