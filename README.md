#magento2setup
## Ubuntu 14.04 LTS

##install
- `source <( curl -s s3.magento2setup.com/ubuntu-14.04-lts-git/bin/getup )`

##install - aws
- Launch EC2 Instance
  - Step 1: Choose AMI
    - `Ubuntu Server 14.04 LTS (HVM), SSD Volume Type - ami-ba3e14d9`
  - Step 2: Choose Instance Type
    - `t2.small+`
  - Step 3: Configure Instance
    - Advanced Details
      - User data
        - `#!/bin/bash`
        - `source <( curl -s s3.magento2setup.com/ubuntu-14.04-lts-git/bin/getup )`
  - Step 4: Add Storage
  - Step 5: Tagg Instance
  - Steo 6: Configure Security Group
    - Add Rule
      - `SSH`
      - `HTTP`
  - Step 7: Review
  - Step 8: Patience...

##install - vagrant
- `cd vagrant && vagrant up`

##note(s)
Uses `ppa:ondrej/php` as Magento 2.x requires PHP5.6+

##version(s)
- `Apache v2.4,2`
- `Magento v2.x`
- `MySQL v14.14 Distrib 5.5.50`
- `PHP v5.6`
