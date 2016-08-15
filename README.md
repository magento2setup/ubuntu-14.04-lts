#magento2 - ubuntu 14.04 lts
Magento 2.1.x running on Ubuntu 14.04 LTS

##installation
- '/bin/bash bin/install'

##note(s)
Uses `ppa:ondrej/php` as Magento 2.1.x requires PHP5.6+

##aws
- Create bucket.
- Launch EC2 Instance
  - Step 1: Choose AMI
    - `Ubuntu Server 14.04 LTS (HVM), SSD Volume Type - ami-ba3e14d9`
  - Step 2: Choose Instance Type
    - `t2.small+`
  - Step 3: Configure Instance
    - Advanced Details
      - User data
        - `bash <( curl -s s3.magento2setup.com/ubuntu-14.04-lts/bin/getup )`
  - Step 4: Add Storage
  - Step 5: Tagg Instance
  - Steo 6: Configure Security Group
    - Add Rule
      - `HTTP`
      - `HTTPS`
  - Step 7: Review
  - Step 8: Patience...


##vagrant
- `cd vagrant && vagrant up`

##version(s)
- PHP `v5.6`
- Magento `v2.1.0`
- MySQL `v14.14 Distrib 5.5.50`
