# AWS Identity and Access Management User Guide

-----
*****Copyright &copy; 2018 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is IAM?](introduction.md)
   + [Understanding How IAM Works](intro-structure.md)
   + [Overview of Identity Management: Users](introduction_identity-management.md)
   + [Overview of Access Management: Permissions and Policies](introduction_access-management.md)
   + [Security Features Outside of IAM](introduction_security-outside-iam.md)
   + [Quick Links to Common Tasks](introduction_quick-links-common-tasks.md)
+ [Getting Set Up](getting-set-up.md)
+ [Getting Started](getting-started.md)
   + [Creating Your First IAM Admin User and Group](getting-started_create-admin-group.md)
   + [How Users Sign In to Your Account](getting-started_how-users-sign-in.md)
+ [IAM Tutorials](tutorials.md)
   + [Tutorial: Delegate Access to the Billing Console](tutorial_billing.md)
   + [Tutorial: Delegate Access Across AWS Accounts Using IAM Roles](tutorial_cross-account-with-roles.md)
   + [Tutorial: Create and Attach Your First Customer Managed Policy](tutorial_managed-policies.md)
   + [Tutorial: Enable Your Users to Configure Their Own Credentials and MFA Settings](tutorial_users-self-manage-mfa-and-creds.md)
+ [IAM Best Practices and Use Cases](IAMBestPracticesAndUseCases.md)
   + [IAM Best Practices](best-practices.md)
   + [Business Use Cases](IAM_UseCases.md)
+ [The IAM Console and Sign-in Page](console.md)
   + [Controlling User Access to the AWS Management Console](console_controlling-access.md)
   + [Your AWS Account ID and Its Alias](console_account-alias.md)
   + [Using MFA Devices With Your IAM Sign-in Page](console_sign-in-mfa.md)
   + [IAM Console Search](console_search.md)
+ [Identities (Users, Groups, and Roles)](id.md)
   + [IAM Users](id_users.md)
      + [Creating an IAM User in Your AWS Account](id_users_create.md)
      + [How IAM Users Sign In to AWS](id_users_sign-in.md)
      + [Managing IAM Users](id_users_manage.md)
      + [Changing Permissions for an IAM User](id_users_change-permissions.md)
      + [Managing Passwords](id_credentials_passwords.md)
         + [Changing the AWS Account Root User Password](id_credentials_passwords_change-root.md)
         + [Setting an Account Password Policy for IAM Users](id_credentials_passwords_account-policy.md)
         + [Managing Passwords for IAM Users](id_credentials_passwords_admin-change-user.md)
         + [Permitting IAM Users to Change Their Own Passwords](id_credentials_passwords_enable-user-change.md)
      + [Managing Access Keys for IAM Users](id_credentials_access-keys.md)
      + [Resetting Your Lost or Forgotten Passwords or Access Keys](id_credentials_access-keys_retrieve.md)
      + [Using Multi-Factor Authentication (MFA) in AWS](id_credentials_mfa.md)
         + [Enabling MFA Devices](id_credentials_mfa_enable.md)
            + [Enabling a Virtual Multi-factor Authentication (MFA) Device](id_credentials_mfa_enable_virtual.md)
            + [Enabling a Hardware MFA Device (Console)](id_credentials_mfa_enable_physical.md)
            + [PREVIEW - Enabling SMS Text Message MFA Devices](id_credentials_mfa_enable_sms.md)
            + [Enable and manage virtual MFA devices (AWS CLI, Tools for Windows PowerShell, or AWS API)](id_credentials_mfa_enable_cliapi.md)
         + [Checking MFA Status](id_credentials_mfa_checking-status.md)
         + [Resynchronize MFA Devices](id_credentials_mfa_sync.md)
         + [Deactivating MFA Devices](id_credentials_mfa_disable.md)
         + [What If an MFA Device Is Lost or Stops Working?](id_credentials_mfa_lost-or-broken.md)
         + [Configuring MFA-Protected API Access](id_credentials_mfa_configure-api-require.md)
         + [Sample Policies with MFA Conditions](id_credentials_mfa_sample-policies.md)
         + [Sample Code: Requesting Credentials with Multi-factor Authentication](id_credentials_mfa_sample-code.md)
      + [Finding Unused Credentials](id_credentials_finding-unused.md)
      + [Getting Credential Reports for Your AWS Account](id_credentials_getting-report.md)
      + [Using IAM with AWS CodeCommit: Git Credentials, SSH Keys, and AWS Access Keys](id_credentials_ssh-keys.md)
      + [Working with Server Certificates](id_credentials_server-certs.md)
   + [IAM Groups](id_groups.md)
      + [Creating IAM Groups](id_groups_create.md)
      + [Managing IAM Groups](id_groups_manage.md)
         + [Listing IAM Groups](id_groups_manage_list.md)
         + [Adding and Removing Users in an IAM Group](id_groups_manage_add-remove-users.md)
         + [Attaching a Policy to an IAM Group](id_groups_manage_attach-policy.md)
         + [Renaming an IAM Group](id_groups_manage_rename.md)
         + [Deleting an IAM Group](id_groups_manage_delete.md)
   + [IAM Roles](id_roles.md)
      + [Roles Terms and Concepts](id_roles_terms-and-concepts.md)
      + [Common Scenarios for Roles: Users, Applications, and Services](id_roles_common-scenarios.md)
         + [Providing Access to an IAM User in Another AWS Account That You Own](id_roles_common-scenarios_aws-accounts.md)
         + [Providing Access to AWS Accounts Owned by Third Parties](id_roles_common-scenarios_third-party.md)
         + [Providing Access to an AWS Service](id_roles_common-scenarios_services.md)
         + [Providing Access to Externally Authenticated Users (Identity Federation)](id_roles_common-scenarios_federated-users.md)
      + [Identity Providers and Federation](id_roles_providers.md)
         + [About Web Identity Federation](id_roles_providers_oidc.md)
            + [Using Amazon Cognito for Mobile Apps](id_roles_providers_oidc_cognito.md)
            + [Using Web Identity Federation APIs for Mobile Apps](id_roles_providers_oidc_manual.md)
            + [Identifying Users with Web Identity Federation](id_roles_providers_oidc_user-id.md)
            + [Additional Resources for Web Identity Federation](id_roles_providers_oidc_resources.md)
         + [About SAML 2.0-based Federation](id_roles_providers_saml.md)
         + [Creating IAM Identity Providers](id_roles_providers_create.md)
            + [Creating OpenID Connect (OIDC) Identity Providers](id_roles_providers_create_oidc.md)
               + [Obtaining the Thumbprint for an OpenID Connect Identity Provider](id_roles_providers_create_oidc_verify-thumbprint.md)
            + [Creating SAML Identity Providers](id_roles_providers_create_saml.md)
               + [Configuring your SAML 2.0 IdP with Relying Party Trust and Adding Claims](id_roles_providers_create_saml_relying-party.md)
               + [Integrating Third-Party SAML Solution Providers with AWS](id_roles_providers_saml_3rd-party.md)
               + [Configuring SAML Assertions for the Authentication Response](id_roles_providers_create_saml_assertions.md)
         + [Enabling SAML 2.0 Federated Users to Access the AWS Management Console](id_roles_providers_enable-console-saml.md)
         + [Creating a URL that Enables Federated Users to Access the AWS Management Console (Custom Federation Broker)](id_roles_providers_enable-console-custom-url.md)
      + [Using Service-Linked Roles](using-service-linked-roles.md)
      + [Creating IAM Roles](id_roles_create.md)
         + [Creating a Role to Delegate Permissions to an IAM User](id_roles_create_for-user.md)
            + [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](id_roles_create_for-user_externalid.md)
         + [Creating a Role to Delegate Permissions to an AWS Service](id_roles_create_for-service.md)
         + [Creating a Role for a Third-Party Identity Provider (Federation)](id_roles_create_for-idp.md)
            + [Creating a Role for Web Identity or OpenID Connect Federation (Console)](id_roles_create_for-idp_oidc.md)
            + [Creating a Role for SAML 2.0 Federation (Console)](id_roles_create_for-idp_saml.md)
         + [Examples of Policies for Delegating Access](id_roles_create_policy-examples.md)
      + [Using IAM Roles](id_roles_use.md)
         + [Granting a User Permissions to Switch Roles](id_roles_use_permissions-to-switch.md)
         + [Granting a User Permissions to Pass a Role to an AWS Service](id_roles_use_passrole.md)
         + [Switching to a Role (AWS Management Console)](id_roles_use_switch-role-console.md)
         + [Switching to an IAM Role (AWS Command Line Interface)](id_roles_use_switch-role-cli.md)
         + [Switching to an IAM Role (Tools for Windows PowerShell)](id_roles_use_switch-role-twp.md)
         + [Switching to an IAM Role (API)](id_roles_use_switch-role-api.md)
         + [Using an IAM Role to Grant Permissions to Applications Running on Amazon EC2 Instances](id_roles_use_switch-role-ec2.md)
            + [Using Instance Profiles](id_roles_use_switch-role-ec2_instance-profiles.md)
         + [Revoking IAM Role Temporary Security Credentials](id_roles_use_revoke-sessions.md)
      + [Managing IAM Roles](id_roles_manage.md)
         + [Modifying a Role](id_roles_manage_modify.md)
         + [Deleting Roles or Instance Profiles](id_roles_manage_delete.md)
      + [How IAM Roles Differ from Resource-based Policies](id_roles_compare-resource-policies.md)
   + [Temporary Security Credentials](id_credentials_temp.md)
      + [Requesting Temporary Security Credentials](id_credentials_temp_request.md)
      + [Using Temporary Security Credentials to Request Access to AWS Resources](id_credentials_temp_use-resources.md)
      + [Controlling Permissions for Temporary Security Credentials](id_credentials_temp_control-access.md)
         + [Permissions for AssumeRole, AssumeRoleWithSAML, and AssumeRoleWithWebIdentity](id_credentials_temp_control-access_assumerole.md)
         + [Permissions for GetFederationToken](id_credentials_temp_control-access_getfederationtoken.md)
         + [Permissions for GetSessionToken](id_credentials_temp_control-access_getsessiontoken.md)
         + [Disabling Permissions for Temporary Security Credentials](id_credentials_temp_control-access_disable-perms.md)
         + [Granting Permissions to Create Temporary Security Credentials](id_credentials_temp_control-access_enable-create.md)
      + [Activating and Deactivating AWS STS in an AWS Region](id_credentials_temp_enable-regions.md)
      + [Sample Applications That Use Temporary Credentials](id_credentials_temp_sample-apps.md)
      + [Additional Resources for Temporary Security Credentials](id_credentials_temp_related-topics.md)
   + [The AWS Account Root User](id_root-user.md)
   + [Logging IAM Events with AWS CloudTrail](cloudtrail-integration.md)
+ [Access Management](access.md)
   + [IAM Policies](access_policies.md)
      + [Managed Policies and Inline Policies](access_policies_managed-vs-inline.md)
         + [Deprecated AWS Managed Policies](access_policies_managed-deprecated.md)
      + [Identity-Based Policies and Resource-Based Policies](access_policies_identity-vs-resource.md)
      + [Controlling Access Using Policies](access_controlling.md)
      + [Example Policies](access_policies_examples.md)
         + [AWS: Allows Access Within Specific Dates](reference_policies_examples_aws-dates.md)
         + [AWS: Allows Specific Access Using MFA Within Specific Dates](reference_policies_examples_aws_mfa-dates.md)
         + [AWS: Denies Access to AWS Based on the Source IP](reference_policies_examples_aws_deny-ip.md)
         + [AWS CodeCommit: Allows Read Access to an AWS CodeCommit Repository, Programmatically and in the Console](reference_policies_examples_codecommit_pull.md)
         + [AWS Data Pipeline: Denies Access to DataPipeline Pipelines That a User Did Not Create](reference_policies_examples_datapipeline_not-owned.md)
         + [Amazon DynamoDB: Allows Access to a Specific Table](reference_policies_examples_dynamodb_specific-table.md)
         + [Amazon DynamoDB: Allows Access to Specific Columns](reference_policies_examples_dynamodb_columns.md)
         + [Amazon DynamoDB: Allows Row-Level Access to DynamoDB Based on an Amazon Cognito ID](reference_policies_examples_dynamodb_rows.md)
         + [Amazon EC2: Allows an EC2 Instance to Attach or Detach Volumes](reference_policies_examples_ec2_volumes-instance.md)
         + [Amazon EC2: Attach or Detach Amazon EBS Volumes to EC2 Instances Based on Tags](reference_policies_examples_ec2_ebs-owner.md)
         + [Amazon EC2: Allows Launching EC2 Instances in a Specific Subnet, Programmatically and in the Console](reference_policies_examples_ec2_instances-subnet.md)
         + [Amazon EC2: Allows Managing EC2 Security Groups Associated With a Specific VPC, Programmatically and in the Console](reference_policies_examples_ec2_securitygroups-vpc.md)
         + [Amazon EC2: Allows Starting or Stopping EC2 Instances a User Has Tagged, Programmatically and in the Console](reference_policies_examples_ec2_tag-owner.md)
         + [Amazon EC2: Allows Full EC2 Access Within a Specific Region, Programmatically and in the Console](reference_policies_examples_ec2_region.md)
         + [Amazon EC2: Allows Starting or Stopping an EC2 Instance and Modifying a Security Group, Programmatically and in the Console](reference_policies_examples_ec2_instance-securitygroup.md)
         + [Amazon EC2: Limits Terminating EC2 Instances to an IP Address Range](reference_policies_examples_ec2_terminate-ip.md)
         + [IAM: Access the Policy Simulator API](reference_policies_examples_iam_policy-sim.md)
         + [IAM: Access the Policy Simulator Console](reference_policies_examples_iam_policy-sim-console.md)
         + [IAM: Access the Policy Simulator API Based on User Path](reference_policies_examples_iam_policy-sim-path.md)
         + [IAM: Access the Policy Simulator Console Based on User Path](reference_policies_examples_iam_policy-sim-path-console.md)
         + [IAM: Allows IAM Users to Self-Manage an MFA Device](reference_policies_examples_iam_mfa-selfmanage.md)
         + [IAM: Allows IAM Users to Rotate Their Own Credentials Programmatically and in the Console](reference_policies_examples_iam_credentials_console.md)
         + [IAM: Limits Managed Policies That Can Be Applied to a New IAM User, Group, or Role](reference_policies_examples_iam_limit-managed.md)
         + [Amazon RDS: Allows Full RDS Database Access Within a Specific Region](reference_policies_examples_rds_region.md)
         + [Amazon RDS: Allows Restoring RDS Databases, Programmatically and In the Console](reference_policies_examples_rds_db-console.md)
         + [Amazon RDS: Allows Tag Owners Full Access to RDS Resources That They Have Tagged](reference_policies_examples_rds_tag-owner.md)
         + [Amazon S3: Allows Amazon Cognito Users to Access Objects in Their Bucket](reference_policies_examples_s3_cognito-bucket.md)
         + [Amazon S3: Allows IAM Users Access to Their S3 Home Directory, Programmatically and In the Console](reference_policies_examples_s3_home-directory-console.md)
         + [Amazon S3: Limits Managing to a Specific S3 Bucket](reference_policies_examples_s3_deny-except-bucket.md)
         + [Amazon S3: Allows Read and Write Access to a Specific S3 Bucket](reference_policies_examples_s3_rw-bucket.md)
         + [Amazon S3: Allows Read and Write Access to a Specific S3 Bucket, Programmatically and in the Console](reference_policies_examples_s3_rw-bucket-console.md)
   + [Managing IAM Policies](access_policies_manage.md)
      + [Creating IAM Policies](access_policies_create.md)
      + [Validating JSON Policies](access_policies_policy-validator.md)
      + [Testing IAM Policies with the IAM Policy Simulator](access_policies_testing-policies.md)
      + [Attaching and Detaching IAM Policies](access_policies_manage-attach-detach.md)
      + [Versioning IAM Policies](access_policies_managed-versioning.md)
      + [Editing IAM Policies](access_policies_manage-edit.md)
      + [Deleting IAM Policies](access_policies_manage-delete.md)
      + [Reducing Policy Scope by Viewing User Activity](access_policies_access-advisor.md)
   + [Understanding Permissions Granted by a Policy](access_policies_understand.md)
      + [Policy Summary (List of Services)](access_policies_understand-policy-summary.md)
         + [Understanding Access Level Summaries Within Policy Summaries](access_policies_understand-policy-summary-access-level-summaries.md)
      + [Service Summary (List of Actions)](access_policies_understand-service-summary.md)
      + [Action Summary (List of Resources)](access_policies_understand-action-summary.md)
      + [Examples of Policy Summaries](access_policies_policy-summary-examples.md)
   + [Permissions Required to Access IAM Resources](access_permissions-required.md)
      + [Example Policies for Administering IAM Resources](id_credentials_delegate-permissions_examples.md)
+ [Troubleshooting IAM](troubleshoot.md)
   + [Troubleshooting General Issues](troubleshoot_general.md)
   + [Troubleshoot IAM Policies](troubleshoot_policies.md)
   + [Troubleshooting IAM Roles](troubleshoot_roles.md)
   + [Troubleshooting Amazon EC2 and IAM](troubleshoot_iam-ec2.md)
   + [Troubleshooting Amazon S3 and IAM](troubleshoot_iam-s3.md)
   + [Troubleshooting SAML 2.0 Federation with AWS](troubleshoot_saml.md)
      + [How to View a SAML Response in Your Browser for Troubleshooting](troubleshoot_saml_view-saml-response.md)
+ [Reference Information for AWS Identity and Access Management](reference.md)
   + [IAM Identifiers](reference_identifiers.md)
   + [Limitations on IAM Entities and Objects](reference_iam-limits.md)
   + [AWS Services That Work with IAM](reference_aws-services-that-work-with-iam.md)
   + [IAM JSON Policy Reference](reference_policies.md)
      + [IAM JSON Policy Elements Reference](reference_policies_elements.md)
         + [IAM JSON Policy Elements: Version](reference_policies_elements_version.md)
         + [IAM JSON Policy Elements: Id](reference_policies_elements_id.md)
         + [IAM JSON Policy Elements: Statement](reference_policies_elements_statement.md)
         + [IAM JSON Policy Elements: Sid](reference_policies_elements_sid.md)
         + [IAM JSON Policy Elements: Effect](reference_policies_elements_effect.md)
         + [IAM JSON Policy Elements: Principal](reference_policies_elements_principal.md)
         + [IAM JSON Policy Elements: NotPrincipal](reference_policies_elements_notprincipal.md)
         + [IAM JSON Policy Elements: Action](reference_policies_elements_action.md)
         + [IAM JSON Policy Elements: NotAction](reference_policies_elements_notaction.md)
         + [IAM JSON Policy Elements: Resource](reference_policies_elements_resource.md)
         + [IAM JSON Policy Elements: NotResource](reference_policies_elements_notresource.md)
         + [IAM JSON Policy Elements: Condition](reference_policies_elements_condition.md)
            + [IAM JSON Policy Elements: Condition Operators](reference_policies_elements_condition_operators.md)
            + [Creating a Condition That Tests Multiple Key Values (Set Operations)](reference_policies_multi-value-conditions.md)
         + [IAM Policy Elements: Variables](reference_policies_variables.md)
         + [IAM JSON Policy Elements: Supported Data Types](reference_policies_elements_datatypes.md)
      + [IAM JSON Policy Evaluation Logic](reference_policies_evaluation-logic.md)
      + [Grammar of the IAM JSON Policy Language](reference_policies_grammar.md)
      + [AWS Managed Policies for Job Functions](access_policies_job-functions.md)
      + [AWS Global and IAM Condition Context Keys](reference_policies_condition-keys.md)
      + [AWS Service Actions and Condition Context Keys for Use in IAM Policies](reference_policies_actionsconditions.md)
         + [Actions and Condition Context Keys for Alexa for Business](list_a4b.md)
         + [Actions and Condition Context Keys for Amazon API Gateway](list_execute-api.md)
         + [Actions and Condition Context Keys for Application Auto Scaling](list_application-autoscaling.md)
         + [Actions and Condition Context Keys for Application Discovery](list_discovery.md)
         + [Actions and Condition Context Keys for Amazon AppStream](list_appstream.md)
         + [Actions and Condition Context Keys for AWS Artifact](list_artifact.md)
         + [Actions and Condition Context Keys for Amazon Athena](list_athena.md)
         + [Actions and Condition Context Keys for Auto Scaling](list_autoscaling.md)
         + [Actions and Condition Context Keys for Auto Scaling Plans](list_autoscaling-plans.md)
         + [Actions and Condition Context Keys for AWS Batch](list_batch.md)
         + [Actions and Condition Context Keys for AWS Billing](list_aws-portal.md)
         + [Actions and Condition Context Keys for AWS Budget Service](list_budgets.md)
         + [Actions and Condition Context Keys for AWS Certificate Manager](list_acm.md)
         + [Actions and Condition Context Keys for Amazon Chime](list_chime.md)
         + [Actions and Condition Context Keys for Amazon AWS Cloud Contact Center](list_connect.md)
         + [Actions and Condition Context Keys for Amazon Cloud Directory](list_clouddirectory.md)
         + [Actions and Condition Context Keys for AWS Cloud9](list_cloud9.md)
         + [Actions and Condition Context Keys for AWS CloudFormation](list_cloudformation.md)
         + [Actions and Condition Context Keys for Amazon CloudFront](list_cloudfront.md)
         + [Actions and Condition Context Keys for AWS CloudHSM](list_cloudhsm.md)
         + [Actions and Condition Context Keys for Amazon CloudSearch](list_cloudsearch.md)
         + [Actions and Condition Context Keys for AWS CloudTrail](list_cloudtrail.md)
         + [Actions and Condition Context Keys for Amazon CloudWatch](list_cloudwatch.md)
         + [Actions and Condition Context Keys for Amazon CloudWatch Events](list_events.md)
         + [Actions and Condition Context Keys for Amazon CloudWatch Logs](list_logs.md)
         + [Actions and Condition Context Keys for AWS Code Signing for Amazon FreeRTOS](list_signer.md)
         + [Actions and Condition Context Keys for AWS CodeBuild](list_codebuild.md)
         + [Actions and Condition Context Keys for AWS CodeCommit](list_codecommit.md)
         + [Actions and Condition Context Keys for AWS CodeDeploy](list_codedeploy.md)
         + [Actions and Condition Context Keys for AWS CodePipeline](list_codepipeline.md)
         + [Actions and Condition Context Keys for AWS CodeStar](list_codestar.md)
         + [Actions and Condition Context Keys for Amazon Cognito Identity](list_cognito-identity.md)
         + [Actions and Condition Context Keys for Amazon Cognito Sync](list_cognito-sync.md)
         + [Actions and Condition Context Keys for Amazon Cognito User Pools](list_cognito-idp.md)
         + [Actions and Condition Context Keys for Amazon Comprehend](list_comprehend.md)
         + [Actions and Condition Context Keys for AWS Config](list_config.md)
         + [Actions and Condition Context Keys for AWS Cost and Usage Report](list_cur.md)
         + [Actions and Condition Context Keys for AWS Cost Explorer Service](list_ce.md)
         + [Actions and Condition Context Keys for Data Pipeline](list_datapipeline.md)
         + [Actions and Condition Context Keys for AWS Database Migration Service](list_dms.md)
         + [Actions and Condition Context Keys for AWS Device Farm](list_devicefarm.md)
         + [Actions and Condition Context Keys for AWS Direct Connect](list_directconnect.md)
         + [Actions and Condition Context Keys for AWS Directory Service](list_ds.md)
         + [Actions and Condition Context Keys for Amazon DynamoDB](list_dynamodb.md)
         + [Actions and Condition Context Keys for Amazon DynamoDB Accelerator (DAX)](list_dax.md)
         + [Actions and Condition Context Keys for Amazon EC2](list_ec2.md)
         + [Actions and Condition Context Keys for Amazon EC2 Container Registry](list_ecr.md)
         + [Actions and Condition Context Keys for Amazon EC2 Container Service](list_ecs.md)
         + [Actions and Condition Context Keys for AWS Elastic Beanstalk](list_elasticbeanstalk.md)
         + [Actions and Condition Context Keys for Amazon Elastic File System](list_elasticfilesystem.md)
         + [Actions and Condition Context Keys for Elastic Load Balancing](list_elasticloadbalancing.md)
         + [Actions and Condition Context Keys for Amazon Elastic MapReduce](list_elasticmapreduce.md)
         + [Actions and Condition Context Keys for Amazon Elastic Transcoder](list_elastictranscoder.md)
         + [Actions and Condition Context Keys for Amazon ElastiCache](list_elasticache.md)
         + [Actions and Condition Context Keys for Amazon Elasticsearch Service](list_es.md)
         + [Actions and Condition Context Keys for AWS Elemental MediaConvert](list_mediaconvert.md)
         + [Actions and Condition Context Keys for AWS Elemental MediaLive](list_medialive.md)
         + [Actions and Condition Context Keys for AWS Elemental MediaPackage](list_mediapackage.md)
         + [Actions and Condition Context Keys for AWS Elemental MediaStore](list_mediastore.md)
         + [Actions and Condition Context Keys for Amazon FreeRTOS](list_freertos.md)
         + [Actions and Condition Context Keys for Amazon GameLift](list_gamelift.md)
         + [Actions and Condition Context Keys for Amazon Glacier](list_glacier.md)
         + [Actions and Condition Context Keys for AWS Glue](list_glue.md)
         + [Actions and Condition Context Keys for AWS Greengrass](list_greengrass.md)
         + [Actions and Condition Context Keys for Amazon GuardDuty](list_guardduty.md)
         + [Actions and Condition Context Keys for AWS Health APIs and Notifications](list_health.md)
         + [Actions and Condition Context Keys for Identity And Access Management](list_iam.md)
         + [Actions and Condition Context Keys for AWS Import Export Disk Service](list_importexport.md)
         + [Actions and Condition Context Keys for Amazon Inspector](list_inspector.md)
         + [Actions and Condition Context Keys for AWS IoT](list_iot.md)
         + [Actions and Condition Context Keys for AWS IoT Analytics](list_iotanalytics.md)
         + [Actions and Condition Context Keys for AWS Key Management Service](list_kms.md)
         + [Actions and Condition Context Keys for Amazon Kinesis](list_kinesis.md)
         + [Actions and Condition Context Keys for Amazon Kinesis Analytics](list_kinesisanalytics.md)
         + [Actions and Condition Context Keys for Amazon Kinesis Firehose](list_firehose.md)
         + [Actions and Condition Context Keys for Amazon Kinesis Video Streams](list_kinesisvideo.md)
         + [Actions and Condition Context Keys for AWS Lambda](list_lambda.md)
         + [Actions and Condition Context Keys for Amazon Lex](list_lex.md)
         + [Actions and Condition Context Keys for Amazon Lightsail](list_lightsail.md)
         + [Actions and Condition Context Keys for Amazon Machine Learning](list_machinelearning.md)
         + [Actions and Condition Context Keys for Manage Amazon API Gateway](list_apigateway.md)
         + [Actions and Condition Context Keys for AWS Marketplace](list_aws-marketplace.md)
         + [Actions and Condition Context Keys for AWS Marketplace Management Portal](list_aws-marketplace-management.md)
         + [Actions and Condition Context Keys for Amazon Mechanical Turk](list_mechanicalturk.md)
         + [Actions and Condition Context Keys for Amazon Mechanical Turk Crowd](list_crowd.md)
         + [Actions and Condition Context Keys for Amazon Message Delivery Service](list_ec2messages.md)
         + [Actions and Condition Context Keys for AWS Migration Hub](list_mgh.md)
         + [Actions and Condition Context Keys for Amazon Mobile Analytics](list_mobileanalytics.md)
         + [Actions and Condition Context Keys for AWS Mobile Hub](list_mobilehub.md)
         + [Actions and Condition Context Keys for Amazon MQ](list_mq.md)
         + [Actions and Condition Context Keys for AWS OpsWorks](list_opsworks.md)
         + [Actions and Condition Context Keys for AWS OpsWorks Configuration Management](list_opsworks-cm.md)
         + [Actions and Condition Context Keys for AWS Organizations](list_organizations.md)
         + [Actions and Condition Context Keys for Amazon Pinpoint](list_mobiletargeting.md)
         + [Actions and Condition Context Keys for Amazon Polly](list_polly.md)
         + [Actions and Condition Context Keys for AWS Price List](list_pricing.md)
         + [Actions and Condition Context Keys for Amazon RDS](list_rds.md)
         + [Actions and Condition Context Keys for Amazon Redshift](list_redshift.md)
         + [Actions and Condition Context Keys for Amazon Rekognition](list_rekognition.md)
         + [Actions and Condition Context Keys for Amazon Resource Group Tagging API](list_tag.md)
         + [Actions and Condition Context Keys for AWS Resource Groups](list_resource-groups.md)
         + [Actions and Condition Context Keys for Amazon Route 53](list_route53.md)
         + [Actions and Condition Context Keys for Amazon Route 53 Auto Naming](list_servicediscovery.md)
         + [Actions and Condition Context Keys for Amazon Route53 Domains](list_route53domains.md)
         + [Actions and Condition Context Keys for Amazon S3](list_s3.md)
         + [Actions and Condition Context Keys for Amazon SageMaker](list_sagemaker.md)
         + [Actions and Condition Context Keys for AWS Security Token Service](list_sts.md)
         + [Actions and Condition Context Keys for AWS Serverless Application Repository](list_serverlessrepo.md)
         + [Actions and Condition Context Keys for AWS Service Catalog](list_servicecatalog.md)
         + [Actions and Condition Context Keys for Amazon SES](list_ses.md)
         + [Actions and Condition Context Keys for AWS Shield](list_shield.md)
         + [Actions and Condition Context Keys for Amazon Simple Systems Manager](list_ssm.md)
         + [Actions and Condition Context Keys for Amazon Simple Workflow Service](list_swf.md)
         + [Actions and Condition Context Keys for Amazon SimpleDB](list_sdb.md)
         + [Actions and Condition Context Keys for Single Sign-On](list_sso.md)
         + [Actions and Condition Context Keys for AWS Snowball](list_snowball.md)
         + [Actions and Condition Context Keys for Amazon SNS](list_sns.md)
         + [Actions and Condition Context Keys for Amazon SQS](list_sqs.md)
         + [Actions and Condition Context Keys for AWS Step Functions](list_states.md)
         + [Actions and Condition Context Keys for Amazon Storage Gateway](list_storagegateway.md)
         + [Actions and Condition Context Keys for AWS Support](list_support.md)
         + [Actions and Condition Context Keys for Amazon Transcribe](list_transcribe.md)
         + [Actions and Condition Context Keys for Amazon Translate](list_translate.md)
         + [Actions and Condition Context Keys for AWS Trusted Advisor](list_trustedadvisor.md)
         + [Actions and Condition Context Keys for AWS WAF](list_waf.md)
         + [Actions and Condition Context Keys for AWS WAF Regional](list_waf-regional.md)
         + [Actions and Condition Context Keys for Amazon WorkDocs](list_workdocs.md)
         + [Actions and Condition Context Keys for Amazon WorkMail](list_workmail.md)
         + [Actions and Condition Context Keys for Amazon WorkSpaces](list_workspaces.md)
         + [Actions and Condition Context Keys for AWS XRay](list_xray.md)
      + [IAM Policy Actions Grouped by Access Level](reference_policies_access-levels.md)
         + [Service Actions Included in the List Access Level](reference_access-level_list.md)
         + [Service Actions Included in the Read Access Level](reference_access-level_read.md)
         + [Service Actions Included in the Write Access Level](reference_access-level_write.md)
         + [Service Actions Included in the Permissions management Access Level](reference_access-level_permissions.md)
+ [Resources](resources.md)
+ [Calling the API by Making HTTP Query Requests](programming.md)
+ [AWS Glossary](glossary.md)