# olm-database

This repo is an automatization for warehousing the redhat operator catalogs images. I try to solve this BZ: https://bugzilla.redhat.com/show_bug.cgi?id=1929775

Every day a job runs to archive the current catalogs images for 
 - 4.5 and 4.6
 - redhat-operators, certified-operators, redhat-marketplace , community-operators

All the images are in QUAY: https://quay.io/repository/mvalledi/olm-cicd , and as commits with files in this repo (one per type for catalog/version) with the list of operators and versions included

Example with structure and relation between catalog list file and container image in this repo:

```
├── 2021
│   └── 02
│       ├── v4.5-certified-operators-202102181515.txt ---> quay.io/mvalledi/olm-cicd:v4.5-certified-operators-202102181515
│       ├── v4.5-certified-operators-202102181527.txt ---> quay.io/mvalledi/olm-cicd:v4.5-certified-operators-202102181527
│       ├── v4.5-community-operators-202102181529.txt ---> quay.io/mvalledi/olm-cicd:v4.5-community-operators-202102181529
│       ├── v4.5-redhat-marketplace-202102181528.txt ---> quay.io/mvalledi/olm-cicd:v4.5-redhat-marketplace-202102181528
│       ├── v4.5-redhat-operators-202102181508.txt ---> quay.io/mvalledi/olm-cicd:v4.5-redhat-operators-202102181508
│       ├── v4.5-redhat-operators-202102181514.txt ---> quay.io/mvalledi/olm-cicd:v4.5-redhat-operators-202102181514
│       ├── v4.5-redhat-operators-202102181525.txt ---> quay.io/mvalledi/olm-cicd:v4.5-redhat-operators-202102181525
│       ├── v4.6-certified-operators-202102181518.txt ---> quay.io/mvalledi/olm-cicd:v4.6-certified-operators-20210218151
│       ├── v4.6-certified-operators-202102181533.txt ---> quay.io/mvalledi/olm-cicd:v4.6-certified-operators-202102181533
│       ├── v4.6-redhat-marketplace-202102181534.txt ---> quay.io/mvalledi/olm-cicd:v4.6-redhat-marketplace-202102181534
│       ├── v4.6-redhat-operators-202102181509.txt ---> quay.io/mvalledi/olm-cicd:v4.6-redhat-operators-202102181509
│       ├── v4.6-redhat-operators-202102181517.txt ---> quay.io/mvalledi/olm-cicd:v4.6-redhat-operators-202102181517
│       └── v4.6-redhat-operators-202102181531.txt ---> quay.io/mvalledi/olm-cicd:v4.6-redhat-operators-202102181531
```

# How to use this repo:
1) Search the operator and version which you are interested in the Github search box in this repo  
2) Find the file in the repo thats includes your "operator:version"
2) Open the file, and in the first line you will fine the operator reference. Example: `# IMAGE: quay.io/mvalledi/olm-cicd:v4.5-certified-operators-202102181515`


