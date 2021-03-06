# Set logging {#concept_lgv_phz_5db .concept}

A large number of access logs are generated when you access OSS. After you enable the logging function for a bucket, OSS automatically records the access logs for the bucket on the hour, write the logs into an object that follows the specified naming convention, and store the object in the target bucket that you specify. For more information, see [Access logging](../../../../reseller.en-US/Developer Guide/Manage logs/访问日志存储.md#) in the OSS developer guide.

**Note:** To ensure that this function works properly, make sure that at least a pair of enabled is available under your account.

## Procedure {#section_nsz_xhz_5db .section}

1.  Log on to the [OSS console](https://partners-intl.console.aliyun.com/#/oss).
2.  In the left-side bucket list, click the name of the bucket that you want to set the logging unction.
3.  Click the **Basic Settings** tab and find the **Log** area.
4.  Click **Configure** and then set **Destination Bucket** and **Log Prefix**.
    -   **Destination Bucket**: In the drop-down list, select the name of the bucket used to store logs. You can only select buckets owned by you and in the same region as the bucket for which the logging function is enabled.
    -   **Log Prefix**: Enter the directory where logs are stored and the prefix of the logs. For example, if you enter log/<TargetPrefix\>, logs are stored in the log/ directory.
5.  Click **Save**.

## Logging naming convention {#section_n4b_q3z_5db .section}

The following example is used to describe the naming convention for objects that store access logs.

<TargetPrefix\><SourceBucket\>YYYY-MM-DD-HH-MM-SS-<UniqueString\>

-   <TargetPrefix\>: Indicates the specified log prefix.
-   <SourceBucket\>: Indicates the name of the source bucket.
-   YYYY-MM-DD-HH-MM-SS: Indicates the time when the log is created, in which YYYY indicates the year, MM indicates the month, DD indicates the day, HH indicates the hour, MM indicates the minute, and SS indicates the second.
-   <UniqueString\>: Indicates a string generated by OSS.

For example, the name of an object used to store OSS access logs is as follows:

MyLog-OSS-example2015-09-10-04-00-00-0000

-   MyLog is the specified log prefix.
-   oss-example is the name of the source bucket.
-   2015-09-10-04-00-00 indicates the time the the log is created.
-   0000 is a string generated by OSS.

