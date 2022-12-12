null_resource.previous: Refreshing state... [id=2249413987220182296]
time_sleep.wait_2_minutes: Refreshing state... [id=2022-12-06T10:55:53Z]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-AppAdmin_group: Refreshing state... [id=2944095046339467|599527370678392]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataScientist_group: Refreshing state... [id=2944095046339467|778674090215959]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-DATALAKE-GIA-AppAdmin_group: Refreshing state... [id=2944095046339467|1053378679920859]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataAnalyst_group: Refreshing state... [id=2944095046339467|702258676958428]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataEngineer_group: Refreshing state... [id=2944095046339467|184927922418731]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DataAnalyst_group: Refreshing state... [id=2944095046339467|208415273553642]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataEngineer_group: Refreshing state... [id=2944095046339467|763693532761156]
databricks_mws_permission_assignment.add_Okta-DBX-E2-CORP-GIA-DATALAKE-DataScientist_group: Refreshing state... [id=2944095046339467|542189264552017]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-AppAdmin: Refreshing state... [id=group/599527370678392]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataScientist: Refreshing state... [id=group/778674090215959]
databricks_instance_profile.corp-de-gia: Refreshing state... [id=arn:aws:iam::671616840389:instance-profile/TEC-EC2-DATABRICKS-DETST-DE-CORP-GIA-ROLE]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataEngineer: Refreshing state... [id=group/184927922418731]
databricks_entitlements.Okta-DBX-E2-CORP-GIA-DataAnalyst: Refreshing state... [id=group/208415273553642]
module.corp-gia-datalake-sql_endpoint.databricks_sql_global_config.template: Refreshing state... [id=global]
module.corp-gia-datalake-sql_endpoint.databricks_sql_endpoint.template: Refreshing state... [id=f9ff6b2230e2056d]
module.corp-gia-sql_endpoint.databricks_sql_global_config.template: Refreshing state... [id=global]
module.corp-gia-sql_endpoint.databricks_sql_endpoint.template: Refreshing state... [id=11ba7cb5a1f9b5f3]
module.corp_de_gia_interactive_cluster.databricks_cluster.template: Refreshing state... [id=1205-153003-qah9ivyd]
module.corp-gia-sql_endpoint.databricks_permissions.template: Refreshing state... [id=/sql/warehouses/11ba7cb5a1f9b5f3]
module.corp-gia-datalake-sql_endpoint.databricks_permissions.template: Refreshing state... [id=/sql/warehouses/f9ff6b2230e2056d]
module.corp_de_gia_interactive_cluster.databricks_permissions.template: Refreshing state... [id=/clusters/1205-153003-qah9ivyd]

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

Plan: 4 to add, 2 to change, 0 to destroy.

─────────────────────────────────────────────────────────────────────────────

Saved the plan to: plan.json
