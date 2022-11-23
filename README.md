Terraform used the selected providers to generate the following execution
plan. Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # databricks_instance_profile.com-ds-gibu will be created
  + resource "databricks_instance_profile" "com-ds-gibu" {
      + id                   = (known after apply)
      + instance_profile_arn = "arn:aws:iam::671616840389:instance-profile/TEC-EC2-DATABRICKS-USTST-DS-COM-GIBU-ROLE"
      + skip_validation      = (known after apply)
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-COM-GIBU-AppAdmin_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-COM-GIBU-AppAdmin_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 765496971411660
      + workspace_id = 1058862015284785
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-COM-GIBU-DataAnalyst_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-COM-GIBU-DataAnalyst_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 108061553014686
      + workspace_id = 1058862015284785
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-COM-GIBU-DataEngineer_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-COM-GIBU-DataEngineer_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 915802239084533
      + workspace_id = 1058862015284785
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-COM-GIBU-DataScientist_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-COM-GIBU-DataScientist_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 115389984835057
      + workspace_id = 1058862015284785
    }

  # module.com_ds-gibu_interactive_cluster.databricks_cluster.template will be created
  + resource "databricks_cluster" "template" {
      + autotermination_minutes      = 120
      + cluster_id                   = (known after apply)
      + cluster_name                 = "DS-COM-GIBU"
      + custom_tags                  = {
          + "ResourceClass"        = "Classic"
          + "Team"                 = "databricks"
          + "account-type"         = "Test"
          + "app"                  = "Gastroenterology Commercial Data Analytics"
          + "application-owner"    = "Mohan.Kuruganti@takeda.com"
          + "business-criticality" = "High"
          + "business-unit-n1"     = "Comm IT"
          + "business-unit-n2"     = "Comm IT-USBU IT"
          + "data-classification"  = "high"
          + "environment-id"       = "Test"
          + "it-business-owner"    = "dl.It_Databricks_Admins@takeda.com"
          + "project-id"           = "APMS-92112"
        }
      + default_tags                 = (known after apply)
      + driver_instance_pool_id      = (known after apply)
      + driver_node_type_id          = "i3.xlarge"
      + enable_elastic_disk          = (known after apply)
      + enable_local_disk_encryption = (known after apply)
      + id                           = (known after apply)
      + node_type_id                 = "i3.xlarge"
      + num_workers                  = 0
      + policy_id                    = "9C6308F7030001C7"
      + spark_conf                   = {
          + "spark.databricks.acl.dfAclsEnabled"                  = "false"
          + "spark.databricks.hive.metastore.glueCatalog.enabled" = "true"
          + "spark.databricks.repl.allowedLanguages"              = "python,sql"
          + "spark.hadoop.aws.glue.cache.db.enable"               = "true"
          + "spark.hadoop.aws.glue.cache.db.size"                 = "1000"
          + "spark.hadoop.aws.glue.cache.db.ttl-mins"             = "30"
          + "spark.hadoop.aws.glue.cache.table.enable"            = "true"
          + "spark.hadoop.aws.glue.cache.table.size"              = "1000"
          + "spark.hadoop.aws.glue.cache.table.ttl-mins"          = "30"
          + "spark.hadoop.fs.s3a.acl.default"                     = "BucketOwnerFullControl"
          + "spark.hadoop.hive.metastore.glue.catalogid"          = "881018545998"
        }
      + spark_version                = "9.1.x-scala2.12"
      + state                        = (known after apply)
      + url                          = (known after apply)

      + autoscale {
          + max_workers = 6
          + min_workers = 1
        }

      + aws_attributes {
          + availability           = "SPOT_WITH_FALLBACK"
          + first_on_demand        = 2
          + instance_profile_arn   = "arn:aws:iam::671616840389:instance-profile/TEC-EC2-DATABRICKS-USTST-DS-COM-GIBU-ROLE"
          + spot_bid_price_percent = 100
          + zone_id                = "auto"
        }
    }

  # module.com_ds-gibu_interactive_cluster.databricks_permissions.template will be created
  + resource "databricks_permissions" "template" {
      + cluster_id  = (known after apply)
      + id          = (known after apply)
      + object_type = (known after apply)

      + access_control {
          + group_name       = "Okta-DBX-E2-COM-GIBU-AppAdmin"
          + permission_level = "CAN_RESTART"
        }
      + access_control {
          + group_name       = "Okta-DBX-E2-COM-GIBU-DataScientist"
          + permission_level = "CAN_RESTART"
        }
    }

Plan: 7 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + com_ds-gibu_interactive_cluster = (known after apply)
