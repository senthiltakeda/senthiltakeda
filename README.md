null_resource.previous: Refreshing state... [id=2249413987220182296]
time_sleep.wait_2_minutes: Refreshing state... [id=2022-12-06T10:55:53Z]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-AppAdmin_group: Refreshing state... [id=2944095046339467|599527370678392]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataEngineer_group: Refreshing state... [id=2944095046339467|184927922418731]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataAnalyst_group: Refreshing state... [id=2944095046339467|208415273553642]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataScientist_group: Refreshing state... [id=2944095046339467|778674090215959]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataEngineer: Refreshing state... [id=group/184927922418731]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataScientist: Refreshing state... [id=group/778674090215959]
databricks_instance_profile.corp-de-gia: Refreshing state... [id=arn:aws:iam::671616840389:instance-profile/TEC-EC2-DATABRICKS-DETST-DE-CORP-GIA-ROLE]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-AppAdmin: Refreshing state... [id=group/599527370678392]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataAnalyst: Refreshing state... [id=group/208415273553642]
module.corp-gia-sql_endpoint.databricks_sql_global_config.template: Refreshing state... [id=global]
module.corp-gia-sql_endpoint.databricks_sql_endpoint.template: Refreshing state... [id=11ba7cb5a1f9b5f3]
module.corp_de_gia_interactive_cluster.databricks_cluster.template: Refreshing state... [id=1205-153003-qah9ivyd]
module.corp_de_gia_interactive_cluster.databricks_permissions.template: Refreshing state... [id=/clusters/1205-153003-qah9ivyd]
module.corp-gia-sql_endpoint.databricks_permissions.template: Refreshing state... [id=/sql/warehouses/11ba7cb5a1f9b5f3]

Note: Objects have changed outside of Terraform

Terraform detected the following changes made outside of Terraform since the
last "terraform apply":

  # module.corp-gia-sql_endpoint.databricks_sql_endpoint.template has changed
  ~ resource "databricks_sql_endpoint" "template" {
        id                        = "11ba7cb5a1f9b5f3"
        name                      = "CORP-GIA-SQL"
      ~ num_clusters              = 1 -> 0
      ~ state                     = "RUNNING" -> "STOPPED"
        # (9 unchanged attributes hidden)


        # (2 unchanged blocks hidden)
    }


Unless you have made equivalent changes to your configuration, or ignored the
relevant attributes using ignore_changes, the following plan may include
actions to undo or respond to these changes.

─────────────────────────────────────────────────────────────────────────────

Terraform used the selected providers to generate the following execution
plan. Resource actions are indicated with the following symbols:
  + create
  ~ update in-place

Terraform will perform the following actions:

  # databricks_entitlements.Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin will be created
  + resource "databricks_entitlements" "Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin" {
      + allow_cluster_create       = false
      + allow_instance_pool_create = false
      + databricks_sql_access      = true
      + group_id                   = "1053378679920859"
      + id                         = (known after apply)
      + workspace_access           = false
    }

  # databricks_entitlements.Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst will be created
  + resource "databricks_entitlements" "Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst" {
      + allow_cluster_create       = false
      + allow_instance_pool_create = false
      + databricks_sql_access      = true
      + group_id                   = "702258676958428"
      + id                         = (known after apply)
      + workspace_access           = false
    }

  # databricks_entitlements.Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer will be created
  + resource "databricks_entitlements" "Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer" {
      + allow_cluster_create       = false
      + allow_instance_pool_create = false
      + databricks_sql_access      = true
      + group_id                   = "763693532761156"
      + id                         = (known after apply)
      + workspace_access           = false
    }

  # databricks_entitlements.Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist will be created
  + resource "databricks_entitlements" "Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist" {
      + allow_cluster_create       = false
      + allow_instance_pool_create = false
      + databricks_sql_access      = true
      + group_id                   = "542189264552017"
      + id                         = (known after apply)
      + workspace_access           = false
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 1053378679920859
      + workspace_id = 2944095046339467
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 702258676958428
      + workspace_id = 2944095046339467
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 763693532761156
      + workspace_id = 2944095046339467
    }

  # databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist_group will be created
  + resource "databricks_mws_permission_assignment" "add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist_group" {
      + id           = (known after apply)
      + permissions  = [
          + "USER",
        ]
      + principal_id = 542189264552017
      + workspace_id = 2944095046339467
    }

  # module.corp-gia-datalake-sql_endpoint.databricks_permissions.template will be created
  + resource "databricks_permissions" "template" {
      + id              = (known after apply)
      + object_type     = (known after apply)
      + sql_endpoint_id = (known after apply)

      + access_control {
          + group_name       = "Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin"
          + permission_level = "CAN_USE"
        }
      + access_control {
          + group_name       = "Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst"
          + permission_level = "CAN_USE"
        }
      + access_control {
          + group_name       = "Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer"
          + permission_level = "CAN_USE"
        }
      + access_control {
          + group_name       = "Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist"
          + permission_level = "CAN_USE"
        }
    }

  # module.corp-gia-datalake-sql_endpoint.databricks_sql_endpoint.template will be created
  + resource "databricks_sql_endpoint" "template" {
      + auto_stop_mins            = 120
      + cluster_size              = "Large"
      + data_source_id            = (known after apply)
      + enable_photon             = true
      + enable_serverless_compute = false
      + id                        = (known after apply)
      + jdbc_url                  = (known after apply)
      + max_num_clusters          = 1
      + min_num_clusters          = 1
      + name                      = "CORP-GIA-DATALAKE-SQL"
      + num_clusters              = 1
      + spot_instance_policy      = "COST_OPTIMIZED"
      + state                     = (known after apply)

      + odbc_params {
          + host     = (known after apply)
          + hostname = (known after apply)
          + path     = (known after apply)
          + port     = (known after apply)
          + protocol = (known after apply)
        }

      + tags {
          + custom_tags {
              + key   = "project-id"
              + value = "APMS-92682"
            }
          + custom_tags {
              + key   = "account-type"
              + value = "production"
            }
          + custom_tags {
              + key   = "Team"
              + value = "admins"
            }
          + custom_tags {
              + key   = "apms-id"
              + value = "APMS-91706"
            }
          + custom_tags {
              + key   = "application-name"
              + value = "databricks"
            }
          + custom_tags {
              + key   = "app"
              + value = "NONE"
            }
          + custom_tags {
              + key   = "it-business-owner"
              + value = "dl.It_Databricks_Admins@takeda.com"
            }
          + custom_tags {
              + key   = "business-criticality"
              + value = "high"
            }
          + custom_tags {
              + key   = "business-unit-n1"
              + value = "CorpIT"
            }
          + custom_tags {
              + key   = "business-unit-n2"
              + value = "CorpIT Corporate Affairs IT"
            }
          + custom_tags {
              + key   = "environment-id"
              + value = "Test"
            }
          + custom_tags {
              + key   = "application-owner"
              + value = "alejandro.castro@takeda.com"
            }
          + custom_tags {
              + key   = "it-technical-owner"
              + value = "dl.Ted-Platform-Team@Takeda.com"
            }
          + custom_tags {
              + key   = "data-classification"
              + value = "confidential"
            }
        }
    }

  # module.corp-gia-datalake-sql_endpoint.databricks_sql_global_config.template will be created
  + resource "databricks_sql_global_config" "template" {
      + data_access_config        = {
          + "spark.databricks.hive.metastore.glueCatalog.enabled" = "true"
          + "spark.hadoop.aws.glue.cache.db.enable"               = "true"
          + "spark.hadoop.aws.glue.cache.db.size"                 = "1000"
          + "spark.hadoop.aws.glue.cache.db.ttl-mins"             = "30"
          + "spark.hadoop.aws.glue.cache.table.enable"            = "true"
          + "spark.hadoop.aws.glue.cache.table.size"              = "1000"
          + "spark.hadoop.aws.glue.cache.table.ttl-mins"          = "30"
          + "spark.hadoop.hive.metastore.glue.catalogid"          = "881018545998"
        }
      + enable_serverless_compute = false
      + id                        = (known after apply)
      + instance_profile_arn      = "arn:aws:iam::671616840389:instance-profile/TEC-EC2-DATABRICKS-JPTSTSQLENDPOINT-ROLE"
      + security_policy           = "DATA_ACCESS_CONTROL"
      + sql_config_params         = {
          + "ANSI_MODE" = "true"
        }
    }

  # module.corp-gia-sql_endpoint.databricks_sql_endpoint.template will be updated in-place
  ~ resource "databricks_sql_endpoint" "template" {
        id                        = "11ba7cb5a1f9b5f3"
        name                      = "CORP-GIA-SQL"
      ~ num_clusters              = 0 -> 1
        # (10 unchanged attributes hidden)


        # (2 unchanged blocks hidden)
    }

  # module.corp_de_gia_interactive_cluster.databricks_cluster.template will be updated in-place
  ~ resource "databricks_cluster" "template" {
      ~ custom_tags                  = {
          - "apms-id"              = "APMS-91706" -> null
          - "application-name"     = "databricks" -> null
          - "it-technical-owner"   = "dl.Ted-Platform-Team@Takeda.com" -> null
          - "ops-exclude-patch"    = "RITM0590559" -> null
            # (12 unchanged elements hidden)
        }
        id                           = "1205-153003-qah9ivyd"
      ~ spark_conf                   = {
          - "spark.databricks.delta.autoCompact.enabled"          = "true" -> null
          - "spark.databricks.delta.optimizeWrite.enabled"        = "true" -> null
            # (11 unchanged elements hidden)
        }
        # (14 unchanged attributes hidden)


        # (2 unchanged blocks hidden)
    }

Plan: 11 to add, 2 to change, 0 to destroy.

─────────────────────────────────────────────────────────────────────────────

Saved the plan to: plan.json

To perform exactly these actions, run the following command to apply:
    terraform apply "plan.json"
