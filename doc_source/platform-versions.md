# Platform Versions<a name="platform-versions"></a>

Amazon EKS platform versions represent the capabilities of the cluster control plane, such as which Kubernetes API server flags are enabled, as well as the current Kubernetes patch version\. Each Kubernetes minor version has one or more associated Amazon EKS platform versions\. The platform versions for different Kubernetes minor versions are independent\.

When a new Kubernetes minor version is available in Amazon EKS, such as 1\.14, the initial Amazon EKS platform version for that Kubernetes minor version starts at `eks.1`\. However, Amazon EKS releases new platform versions periodically to enable new Kubernetes control plane settings and to provide security fixes\.

When new Amazon EKS platform versions become available for a minor version:
+ The Amazon EKS platform version number is incremented \(`eks.n+1`\)\.
+ Amazon EKS automatically upgrades all existing clusters to the latest Amazon EKS platform version for their corresponding Kubernetes minor version\.
+ Amazon EKS might publish a new worker AMI with a corresponding patch version\. However, all patch versions are compatible between the EKS control plane and worker AMIs for a given Kubernetes minor version\.

 New Amazon EKS platform versions don't introduce breaking changes or cause service interruptions\. 

**Note**  
Automatic upgrades of existing Amazon EKS platform versions are rolled out incrementally\. The roll\-out process might take some time\. If you need the latest Amazon EKS platform version features immediately, you should create a new Amazon EKS cluster\.

Clusters are always created with the latest available Amazon EKS platform version \(`eks.n`\) for the specified Kubernetes version\. If you update your cluster to a new Kubernetes minor version, your cluster receives the current Amazon EKS platform version for the Kubernetes minor version that you updated to\.

The current and recent Amazon EKS platform versions are described in the following tables\.

## Kubernetes version 1\.14<a name="platform-versions-1.14"></a>


| Kubernetes Version | Amazon EKS Platform Version | Enabled Admission Controllers | Release Notes | 
| --- | --- | --- | --- | 
| 1\.14\.6 | eks\.1 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook, PodSecurityPolicy | Initial release of Kubernetes 1\.14 for Amazon EKS\. For more information, see [Kubernetes 1\.14](kubernetes-versions.md#kubernetes-1.14)\. | 

## Kubernetes version 1\.13<a name="platform-versions-1.13"></a>


| Kubernetes Version | Amazon EKS Platform Version | Enabled Admission Controllers | Release Notes | 
| --- | --- | --- | --- | 
| 1\.13\.10 | eks\.4 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook, PodSecurityPolicy | New platform version to support IAM roles for service accounts\. For more information, see [IAM Roles for Service Accounts](iam-roles-for-service-accounts.md)\. | 
| 1\.13\.10 | eks\.3 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook, PodSecurityPolicy | New platform version updating Amazon EKS Kubernetes 1\.13 clusters to a patched version of 1\.13\.10 to address [CVE\-2019\-9512 and CVE\-2019\-9514](https://groups.google.com/forum/#!topic/kubernetes-security-announce/wlHLHit1BqA)\. | 
| 1\.13\.8 | eks\.2 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook, PodSecurityPolicy | New platform version updating Amazon EKS Kubernetes 1\.13 clusters to a patched version of 1\.13\.8 to address [CVE\-2019\-11247 and CVE\-2019\-11249](https://groups.google.com/forum/#!topic/kubernetes-security-announce/vUtEcSEY6SM)\. | 
| 1\.13\.7 | eks\.1 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook, PodSecurityPolicy | Initial release of Kubernetes 1\.13 for Amazon EKS\. For more information, see [Kubernetes 1\.13](kubernetes-versions.md#kubernetes-1.13)\. | 

## Kubernetes version 1\.12<a name="platform-versions-1.12"></a>


| Kubernetes Version | Amazon EKS Platform Version | Enabled Admission Controllers | Release Notes | 
| --- | --- | --- | --- | 
| 1\.12\.10 | eks\.4 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Amazon EKS Kubernetes 1\.12 clusters to a patched version of 1\.12\.10 to address [CVE\-2019\-9512 and CVE\-2019\-9514](https://groups.google.com/forum/#!topic/kubernetes-security-announce/wlHLHit1BqA)\. | 
| 1\.12\.10 | eks\.3 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Amazon EKS Kubernetes 1\.12 clusters to a patched version of 1\.12\.10 to address [CVE\-2019\-11247 and CVE\-2019\-11249](https://groups.google.com/forum/#!topic/kubernetes-security-announce/vUtEcSEY6SM)\. | 
| 1\.12\.6 | eks\.2 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version to support custom DNS names in the Kubelet certificate and improve etcd performance\. This fixes a bug that caused worker node Kubelet daemons to request a new certificate every few seconds\. | 
| 1\.12\.6 | eks\.1 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | Initial release of Kubernetes 1\.12 for Amazon EKS\. | 

## Kubernetes version 1\.11<a name="platform-versions-1.11"></a>


| Kubernetes Version | Amazon EKS Platform Version | Enabled Admission Controllers | Release Notes | 
| --- | --- | --- | --- | 
| 1\.11\.10 | eks\.5 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Amazon EKS Kubernetes 1\.11 clusters to a patched version of 1\.11\.10 to address [CVE\-2019\-9512 and CVE\-2019\-9514](https://groups.google.com/forum/#!topic/kubernetes-security-announce/wlHLHit1BqA)\. | 
| 1\.11\.10 | eks\.4 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Amazon EKS Kubernetes 1\.11 clusters to a patched version of 1\.11\.10 to address [CVE\-2019\-11247 and CVE\-2019\-11249](https://groups.google.com/forum/#!topic/kubernetes-security-announce/vUtEcSEY6SM)\. | 
| 1\.11\.8 | eks\.3 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version to support custom DNS names in the Kubelet certificate and improve etcd performance\. | 
| 1\.11\.8 | eks\.2 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Amazon EKS Kubernetes 1\.11 clusters to patch level 1\.11\.8 to address [CVE\-2019\-1002100](https://discuss.kubernetes.io/t/kubernetes-security-announcement-v1-11-8-1-12-6-1-13-4-released-to-address-medium-severity-cve-2019-1002100/5147)\. | 
| 1\.11\.5 | eks\.1 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | Initial release of Kubernetes 1\.11 for Amazon EKS\. | 

## Kubernetes version 1\.10<a name="platform-versions-1.10"></a>

**Important**  
Amazon EKS will deprecate Kubernetes version 1\.11 on November 4th, 2019\. On this day, you will no longer be able to create new 1\.11 clusters, and all Amazon EKS clusters running Kubernetes version 1\.11 will be updated to the latest available platform version of Kubernetes version 1\.12\. For more information, see [Amazon EKS Version Deprecation](kubernetes-versions.md#version-deprecation)\.  
Kubernetes version 1\.10 is no longer supported on Amazon EKS\. You can no longer create new 1\.10 clusters, and all existing Amazon EKS clusters running Kubernetes version 1\.10 will eventually be automatically updated to the latest available platform version of Kubernetes version 1\.11\. For more information, see [Amazon EKS Version Deprecation](kubernetes-versions.md#version-deprecation)\.  
Please update any 1\.10 clusters to version 1\.11 or higher in order to avoid service interruption\. For more information, see [Updating an Amazon EKS Cluster Kubernetes Version](update-cluster.md)\.


| Kubernetes Version | Amazon EKS Platform Version | Enabled Admission Controllers | Release Notes | 
| --- | --- | --- | --- | 
| 1\.10\.13 | eks\.5 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version to support custom DNS names in the Kubelet certificate and improve etcd performance\. Updated to GitVersion:"v1\.10\.13\-eks\-4a9600" to address [CVE\-2019\-11247 and CVE\-2019\-11249](https://groups.google.com/forum/#!topic/kubernetes-security-announce/vUtEcSEY6SM)\. | 
| 1\.10\.13 | eks\.4 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Kubernetes to patch level 1\.10\.13 and a patch to address [CVE\-2019\-1002100](https://discuss.kubernetes.io/t/kubernetes-security-announcement-v1-11-8-1-12-6-1-13-4-released-to-address-medium-severity-cve-2019-1002100/5147)\. | 
| 1\.10\.11 | eks\.3 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook | New platform version updating Kubernetes to patch level 1\.10\.11 to address [CVE\-2018\-1002105](https://aws.amazon.com/security/security-bulletins/AWS-2018-020/)\. | 
| 1\.10\.3 | eks\.2 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction, MutatingAdmissionWebhook, ValidatingAdmissionWebhook |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/eks/latest/userguide/platform-versions.html)  | 
| 1\.10\.3 | eks\.1 | ​NamespaceLifecycle, LimitRanger, ServiceAccount, DefaultStorageClass, ResourceQuota, DefaultTolerationSeconds, NodeRestriction | Initial launch of Amazon EKS\. | 