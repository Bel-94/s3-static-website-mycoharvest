# 🍄 MycoHarvest — Static Website on Amazon S3

A production-ready static marketing site for **MycoHarvest** (organic mushrooms, microgreens & sprouts) hosted on **Amazon S3**.  

<!-- Optional enhancements include **CloudFront** for HTTPS + CDN and **Route 53** for a custom domain. -->

> **Live Demo:** https://YOUR-S3-WEBSITE-ENDPOINT  
*(replace with your real S3 website URL)*

---

## 🎯 Project Goals
- Publish a fast, low-cost static site (HTML/CSS/JS) for MycoHarvest.
- Document S3 Static Website Hosting end-to-end.
- (Optional) Add CloudFront + Route 53 for HTTPS and a custom domain.

---

## 🏗️ Architecture

```mermaid
flowchart LR
  User((User)) -->|HTTP/HTTPS| CF[CloudFront CDN]
  CF --> S3[S3 Static Website Bucket]

  classDef dim fill:#f5f5f5,stroke:#bbb,color:#333;
  class S3,CF dim;


NB: If you skip CloudFront, users hit the S3 Website Endpoint directly (HTTP only).
To get HTTPS, place CloudFront in front of S3.