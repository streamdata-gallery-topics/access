---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 0
info:
  title: Amazon Redshift API Modify Cluster Iam Roles
  version: 1.0.0
  description: |-
    Modifies the list of AWS Identity and Access Management (IAM) roles that can be
                used by the cluster to access other AWS services.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AuthorizeSnapshotAccess:
    get:
      summary: Authorize Snapshot Access
      description: |-
        Authorizes the specified AWS customer account to restore the specified
                    snapshot.
      operationId: authorizeSnapshotAccess
      x-api-path-slug: actionauthorizesnapshotaccess-get
      parameters:
      - in: query
        name: AccountWithRestoreAccess
        description: The identifier of the AWS customer account authorized to restore
          the specified            snapshot
        type: string
      - in: query
        name: SnapshotClusterIdentifier
        description: The identifier of the cluster the snapshot was created from
        type: string
      - in: query
        name: SnapshotIdentifier
        description: The identifier of the snapshot the account is authorized to restore
        type: string
      responses:
        200:
          description: OK
      tags:
      - Snapshots
  /?Action=ModifyClusterIamRoles:
    get:
      summary: Modify Cluster Iam Roles
      description: |-
        Modifies the list of AWS Identity and Access Management (IAM) roles that can be
                    used by the cluster to access other AWS services.
      operationId: modifyClusterIamRoles
      x-api-path-slug: actionmodifyclusteriamroles-get
      parameters:
      - in: query
        name: AddIamRoles.IamRoleArn.N
        description: Zero or more IAM roles to associate with the cluster
        type: string
      - in: query
        name: ClusterIdentifier
        description: The unique identifier of the cluster for which you want to associate
          or            disassociate IAM roles
        type: string
      - in: query
        name: RemoveIamRoles.IamRoleArn.N
        description: Zero or more IAM roles in ARN format to disassociate from the
          cluster
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster IAM Roles
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---