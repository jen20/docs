---
title: Module dms
---

<a href="../index.html">@pulumi/aws</a> &gt; dms

<h2 class="pdoc-module-header">Index</h2>

* <a href="#Certificate">class Certificate</a>
* <a href="#Endpoint">class Endpoint</a>
* <a href="#ReplicationInstance">class ReplicationInstance</a>
* <a href="#ReplicationSubnetGroup">class ReplicationSubnetGroup</a>
* <a href="#ReplicationTask">class ReplicationTask</a>
* <a href="#CertificateArgs">interface CertificateArgs</a>
* <a href="#CertificateState">interface CertificateState</a>
* <a href="#EndpointArgs">interface EndpointArgs</a>
* <a href="#EndpointState">interface EndpointState</a>
* <a href="#ReplicationInstanceArgs">interface ReplicationInstanceArgs</a>
* <a href="#ReplicationInstanceState">interface ReplicationInstanceState</a>
* <a href="#ReplicationSubnetGroupArgs">interface ReplicationSubnetGroupArgs</a>
* <a href="#ReplicationSubnetGroupState">interface ReplicationSubnetGroupState</a>
* <a href="#ReplicationTaskArgs">interface ReplicationTaskArgs</a>
* <a href="#ReplicationTaskState">interface ReplicationTaskState</a>

<a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts">dms/certificate.ts</a> <a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts">dms/endpoint.ts</a> <a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts">dms/replicationInstance.ts</a> <a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts">dms/replicationSubnetGroup.ts</a> <a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts">dms/replicationTask.ts</a> 


<h2 class="pdoc-module-header" id="Certificate">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L12">class Certificate</a>
</h2>

Provides a DMS (Data Migration Service) certificate resource. DMS certificates can be created, deleted, and imported.

~> **Note:** All arguments including the PEM encoded certificate will be stored in the raw state as plain-text.
[Read more about sensitive data in state](/docs/state/sensitive-data.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L40">constructor</a>
</h3>

```typescript
new Certificate(name: string, args: CertificateArgs, opts?: pulumi.CustomResourceOptions)
```


Create a Certificate resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L21">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: CertificateState): Certificate
```


Get an existing Certificate resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L28">property certificateArn</a>
</h3>

```typescript
public certificateArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the certificate.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L32">property certificateId</a>
</h3>

```typescript
public certificateId: pulumi.Output<string>;
```


The certificate identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L36">property certificatePem</a>
</h3>

```typescript
public certificatePem: pulumi.Output<string | undefined>;
```


The contents of the .pem X.509 certificate file for the certificate. Either `certificate_pem` or `certificate_wallet` must be set.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L40">property certificateWallet</a>
</h3>

```typescript
public certificateWallet: pulumi.Output<string | undefined>;
```


The contents of the Oracle Wallet certificate for use with SSL. Either `certificate_pem` or `certificate_wallet` must be set.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h2 class="pdoc-module-header" id="Endpoint">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L14">class Endpoint</a>
</h2>

Provides a DMS (Data Migration Service) endpoint resource. DMS endpoints can be created, updated, deleted, and imported.

~> **Note:** All arguments including the password will be stored in the raw state as plain-text.
[Read more about sensitive data in state](/docs/state/sensitive-data.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L94">constructor</a>
</h3>

```typescript
new Endpoint(name: string, args: EndpointArgs, opts?: pulumi.CustomResourceOptions)
```


Create a Endpoint resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L23">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: EndpointState): Endpoint
```


Get an existing Endpoint resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L30">property certificateArn</a>
</h3>

```typescript
public certificateArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the certificate.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L34">property databaseName</a>
</h3>

```typescript
public databaseName: pulumi.Output<string | undefined>;
```


The name of the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L38">property endpointArn</a>
</h3>

```typescript
public endpointArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L42">property endpointId</a>
</h3>

```typescript
public endpointId: pulumi.Output<string>;
```


The database endpoint identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L46">property endpointType</a>
</h3>

```typescript
public endpointType: pulumi.Output<string>;
```


The type of endpoint. Can be one of `source | target`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L50">property engineName</a>
</h3>

```typescript
public engineName: pulumi.Output<string>;
```


The type of engine for the endpoint. Can be one of `mysql | oracle | postgres | mariadb | aurora | redshift | sybase | sqlserver | dynamodb | mongodb | s3 | azuredb`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L54">property extraConnectionAttributes</a>
</h3>

```typescript
public extraConnectionAttributes: pulumi.Output<string>;
```


Additional attributes associated with the connection. For available attributes see [Using Extra Connection Attributes with AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.ConnectionAttributes.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L58">property kmsKeyArn</a>
</h3>

```typescript
public kmsKeyArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L62">property mongodbSettings</a>
</h3>

```typescript
public mongodbSettings: pulumi.Output<{ ... } | undefined>;
```


Settings for the source MongoDB endpoint. Available settings are `auth_type` (default: `PASSWORD`), `auth_mechanism` (default: `DEFAULT`), `nesting_level` (default: `NONE`), `extract_doc_id` (default: `false`), `docs_to_investigate` (default: `1000`) and `auth_source` (default: `admin`). For more details, see [Using MongoDB as a Source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L66">property password</a>
</h3>

```typescript
public password: pulumi.Output<string | undefined>;
```


The password to be used to login to the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L70">property port</a>
</h3>

```typescript
public port: pulumi.Output<number | undefined>;
```


The port used by the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L74">property s3Settings</a>
</h3>

```typescript
public s3Settings: pulumi.Output<{ ... } | undefined>;
```


Settings for the target S3 endpoint. Available settings are `service_access_role_arn`, `external_table_definition`, `csv_row_delimiter` (default: `\\n`), `csv_delimiter` (default: `,`), `bucket_folder`, `bucket_name` and `compression_type` (default: `NONE`). For more details, see [Using Amazon S3 as a Target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L78">property serverName</a>
</h3>

```typescript
public serverName: pulumi.Output<string | undefined>;
```


The host name of the server.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L82">property serviceAccessRole</a>
</h3>

```typescript
public serviceAccessRole: pulumi.Output<string | undefined>;
```


The Amazon Resource Name (ARN) used by the service access IAM role for dynamodb endpoints.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L86">property sslMode</a>
</h3>

```typescript
public sslMode: pulumi.Output<string>;
```


The SSL mode to use for the connection. Can be one of `none | require | verify-ca | verify-full`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L90">property tags</a>
</h3>

```typescript
public tags: pulumi.Output<Tags | undefined>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L94">property username</a>
</h3>

```typescript
public username: pulumi.Output<string | undefined>;
```


The user name to be used to login to the endpoint database.

<h2 class="pdoc-module-header" id="ReplicationInstance">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L11">class ReplicationInstance</a>
</h2>

Provides a DMS (Data Migration Service) replication instance resource. DMS replication instances can be created, updated, deleted, and imported.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L91">constructor</a>
</h3>

```typescript
new ReplicationInstance(name: string, args: ReplicationInstanceArgs, opts?: pulumi.CustomResourceOptions)
```


Create a ReplicationInstance resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L20">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: ReplicationInstanceState): ReplicationInstance
```


Get an existing ReplicationInstance resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L27">property allocatedStorage</a>
</h3>

```typescript
public allocatedStorage: pulumi.Output<number>;
```


The amount of storage (in gigabytes) to be initially allocated for the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L31">property applyImmediately</a>
</h3>

```typescript
public applyImmediately: pulumi.Output<boolean | undefined>;
```


Indicates whether the changes should be applied immediately or during the next maintenance window. Only used when updating an existing resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L35">property autoMinorVersionUpgrade</a>
</h3>

```typescript
public autoMinorVersionUpgrade: pulumi.Output<boolean>;
```


Indicates that minor engine upgrades will be applied automatically to the replication instance during the maintenance window.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L39">property availabilityZone</a>
</h3>

```typescript
public availabilityZone: pulumi.Output<string>;
```


The EC2 Availability Zone that the replication instance will be created in.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L43">property engineVersion</a>
</h3>

```typescript
public engineVersion: pulumi.Output<string>;
```


The engine version number of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L47">property kmsKeyArn</a>
</h3>

```typescript
public kmsKeyArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L51">property multiAz</a>
</h3>

```typescript
public multiAz: pulumi.Output<boolean>;
```


Specifies if the replication instance is a multi-az deployment. You cannot set the `availability_zone` parameter if the `multi_az` parameter is set to `true`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L55">property preferredMaintenanceWindow</a>
</h3>

```typescript
public preferredMaintenanceWindow: pulumi.Output<string>;
```


The weekly time range during which system maintenance can occur, in Universal Coordinated Time (UTC).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L59">property publiclyAccessible</a>
</h3>

```typescript
public publiclyAccessible: pulumi.Output<boolean>;
```


Specifies the accessibility options for the replication instance. A value of true represents an instance with a public IP address. A value of false represents an instance with a private IP address.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L63">property replicationInstanceArn</a>
</h3>

```typescript
public replicationInstanceArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L67">property replicationInstanceClass</a>
</h3>

```typescript
public replicationInstanceClass: pulumi.Output<string>;
```


The compute and memory capacity of the replication instance as specified by the replication instance class. Can be one of `dms.t2.micro | dms.t2.small | dms.t2.medium | dms.t2.large | dms.c4.large | dms.c4.xlarge | dms.c4.2xlarge | dms.c4.4xlarge`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L71">property replicationInstanceId</a>
</h3>

```typescript
public replicationInstanceId: pulumi.Output<string>;
```


The replication instance identifier. This parameter is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L75">property replicationInstancePrivateIps</a>
</h3>

```typescript
public replicationInstancePrivateIps: pulumi.Output<string[]>;
```


A list of the private IP addresses of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L79">property replicationInstancePublicIps</a>
</h3>

```typescript
public replicationInstancePublicIps: pulumi.Output<string[]>;
```


A list of the public IP addresses of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L83">property replicationSubnetGroupId</a>
</h3>

```typescript
public replicationSubnetGroupId: pulumi.Output<string>;
```


A subnet group to associate with the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L87">property tags</a>
</h3>

```typescript
public tags: pulumi.Output<Tags | undefined>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L91">property vpcSecurityGroupIds</a>
</h3>

```typescript
public vpcSecurityGroupIds: pulumi.Output<string[]>;
```


A list of VPC security group IDs to be used with the replication instance. The VPC security groups must work with the VPC containing the replication instance.

<h2 class="pdoc-module-header" id="ReplicationSubnetGroup">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L11">class ReplicationSubnetGroup</a>
</h2>

Provides a DMS (Data Migration Service) replication subnet group resource. DMS replication subnet groups can be created, updated, deleted, and imported.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L44">constructor</a>
</h3>

```typescript
new ReplicationSubnetGroup(name: string, args: ReplicationSubnetGroupArgs, opts?: pulumi.CustomResourceOptions)
```


Create a ReplicationSubnetGroup resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L20">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: ReplicationSubnetGroupState): ReplicationSubnetGroup
```


Get an existing ReplicationSubnetGroup resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L24">property replicationSubnetGroupArn</a>
</h3>

```typescript
public replicationSubnetGroupArn: pulumi.Output<string>;
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L28">property replicationSubnetGroupDescription</a>
</h3>

```typescript
public replicationSubnetGroupDescription: pulumi.Output<string>;
```


The description for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L32">property replicationSubnetGroupId</a>
</h3>

```typescript
public replicationSubnetGroupId: pulumi.Output<string>;
```


The name for the replication subnet group. This value is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L36">property subnetIds</a>
</h3>

```typescript
public subnetIds: pulumi.Output<string[]>;
```


A list of the EC2 subnet IDs for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L40">property tags</a>
</h3>

```typescript
public tags: pulumi.Output<Tags | undefined>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L44">property vpcId</a>
</h3>

```typescript
public vpcId: pulumi.Output<string>;
```


The ID of the VPC the subnet group is in.

<h2 class="pdoc-module-header" id="ReplicationTask">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L11">class ReplicationTask</a>
</h2>

Provides a DMS (Data Migration Service) replication task resource. DMS replication tasks can be created, updated, deleted, and imported.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L63">constructor</a>
</h3>

```typescript
new ReplicationTask(name: string, args: ReplicationTaskArgs, opts?: pulumi.CustomResourceOptions)
```


Create a ReplicationTask resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L20">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: ReplicationTaskState): ReplicationTask
```


Get an existing ReplicationTask resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L27">property cdcStartTime</a>
</h3>

```typescript
public cdcStartTime: pulumi.Output<string | undefined>;
```


The Unix timestamp integer for the start of the Change Data Capture (CDC) operation.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L31">property migrationType</a>
</h3>

```typescript
public migrationType: pulumi.Output<string>;
```


The migration type. Can be one of `full-load | cdc | full-load-and-cdc`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L35">property replicationInstanceArn</a>
</h3>

```typescript
public replicationInstanceArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L39">property replicationTaskArn</a>
</h3>

```typescript
public replicationTaskArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) for the replication task.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L43">property replicationTaskId</a>
</h3>

```typescript
public replicationTaskId: pulumi.Output<string>;
```


The replication task identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L47">property replicationTaskSettings</a>
</h3>

```typescript
public replicationTaskSettings: pulumi.Output<string | undefined>;
```


An escaped JSON string that contains the task settings. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L51">property sourceEndpointArn</a>
</h3>

```typescript
public sourceEndpointArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the source endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L55">property tableMappings</a>
</h3>

```typescript
public tableMappings: pulumi.Output<string>;
```


An escaped JSON string that contains the table mappings. For information on table mapping see [Using Table Mapping with an AWS Database Migration Service Task to Select and Filter Data](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TableMapping.html)

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L59">property tags</a>
</h3>

```typescript
public tags: pulumi.Output<Tags | undefined>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L63">property targetEndpointArn</a>
</h3>

```typescript
public targetEndpointArn: pulumi.Output<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the target endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h2 class="pdoc-module-header" id="CertificateArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L97">interface CertificateArgs</a>
</h2>

The set of arguments for constructing a Certificate resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L101">property certificateId</a>
</h3>

```typescript
certificateId: pulumi.Input<string>;
```


The certificate identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L105">property certificatePem</a>
</h3>

```typescript
certificatePem?: pulumi.Input<string>;
```


The contents of the .pem X.509 certificate file for the certificate. Either `certificate_pem` or `certificate_wallet` must be set.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L109">property certificateWallet</a>
</h3>

```typescript
certificateWallet?: pulumi.Input<string>;
```


The contents of the Oracle Wallet certificate for use with SSL. Either `certificate_pem` or `certificate_wallet` must be set.

<h2 class="pdoc-module-header" id="CertificateState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L75">interface CertificateState</a>
</h2>

Input properties used for looking up and filtering Certificate resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L79">property certificateArn</a>
</h3>

```typescript
certificateArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the certificate.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L83">property certificateId</a>
</h3>

```typescript
certificateId?: pulumi.Input<string>;
```


The certificate identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L87">property certificatePem</a>
</h3>

```typescript
certificatePem?: pulumi.Input<string>;
```


The contents of the .pem X.509 certificate file for the certificate. Either `certificate_pem` or `certificate_wallet` must be set.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/certificate.ts#L91">property certificateWallet</a>
</h3>

```typescript
certificateWallet?: pulumi.Input<string>;
```


The contents of the Oracle Wallet certificate for use with SSL. Either `certificate_pem` or `certificate_wallet` must be set.

<h2 class="pdoc-module-header" id="EndpointArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L235">interface EndpointArgs</a>
</h2>

The set of arguments for constructing a Endpoint resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L239">property certificateArn</a>
</h3>

```typescript
certificateArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the certificate.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L243">property databaseName</a>
</h3>

```typescript
databaseName?: pulumi.Input<string>;
```


The name of the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L247">property endpointId</a>
</h3>

```typescript
endpointId: pulumi.Input<string>;
```


The database endpoint identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L251">property endpointType</a>
</h3>

```typescript
endpointType: pulumi.Input<string>;
```


The type of endpoint. Can be one of `source | target`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L255">property engineName</a>
</h3>

```typescript
engineName: pulumi.Input<string>;
```


The type of engine for the endpoint. Can be one of `mysql | oracle | postgres | mariadb | aurora | redshift | sybase | sqlserver | dynamodb | mongodb | s3 | azuredb`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L259">property extraConnectionAttributes</a>
</h3>

```typescript
extraConnectionAttributes?: pulumi.Input<string>;
```


Additional attributes associated with the connection. For available attributes see [Using Extra Connection Attributes with AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.ConnectionAttributes.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L263">property kmsKeyArn</a>
</h3>

```typescript
kmsKeyArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L267">property mongodbSettings</a>
</h3>

```typescript
mongodbSettings?: pulumi.Input<{ ... }>;
```


Settings for the source MongoDB endpoint. Available settings are `auth_type` (default: `PASSWORD`), `auth_mechanism` (default: `DEFAULT`), `nesting_level` (default: `NONE`), `extract_doc_id` (default: `false`), `docs_to_investigate` (default: `1000`) and `auth_source` (default: `admin`). For more details, see [Using MongoDB as a Source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L271">property password</a>
</h3>

```typescript
password?: pulumi.Input<string>;
```


The password to be used to login to the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L275">property port</a>
</h3>

```typescript
port?: pulumi.Input<number>;
```


The port used by the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L279">property s3Settings</a>
</h3>

```typescript
s3Settings?: pulumi.Input<{ ... }>;
```


Settings for the target S3 endpoint. Available settings are `service_access_role_arn`, `external_table_definition`, `csv_row_delimiter` (default: `\\n`), `csv_delimiter` (default: `,`), `bucket_folder`, `bucket_name` and `compression_type` (default: `NONE`). For more details, see [Using Amazon S3 as a Target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L283">property serverName</a>
</h3>

```typescript
serverName?: pulumi.Input<string>;
```


The host name of the server.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L287">property serviceAccessRole</a>
</h3>

```typescript
serviceAccessRole?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) used by the service access IAM role for dynamodb endpoints.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L291">property sslMode</a>
</h3>

```typescript
sslMode?: pulumi.Input<string>;
```


The SSL mode to use for the connection. Can be one of `none | require | verify-ca | verify-full`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L295">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L299">property username</a>
</h3>

```typescript
username?: pulumi.Input<string>;
```


The user name to be used to login to the endpoint database.

<h2 class="pdoc-module-header" id="EndpointState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L161">interface EndpointState</a>
</h2>

Input properties used for looking up and filtering Endpoint resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L165">property certificateArn</a>
</h3>

```typescript
certificateArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the certificate.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L169">property databaseName</a>
</h3>

```typescript
databaseName?: pulumi.Input<string>;
```


The name of the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L173">property endpointArn</a>
</h3>

```typescript
endpointArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L177">property endpointId</a>
</h3>

```typescript
endpointId?: pulumi.Input<string>;
```


The database endpoint identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L181">property endpointType</a>
</h3>

```typescript
endpointType?: pulumi.Input<string>;
```


The type of endpoint. Can be one of `source | target`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L185">property engineName</a>
</h3>

```typescript
engineName?: pulumi.Input<string>;
```


The type of engine for the endpoint. Can be one of `mysql | oracle | postgres | mariadb | aurora | redshift | sybase | sqlserver | dynamodb | mongodb | s3 | azuredb`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L189">property extraConnectionAttributes</a>
</h3>

```typescript
extraConnectionAttributes?: pulumi.Input<string>;
```


Additional attributes associated with the connection. For available attributes see [Using Extra Connection Attributes with AWS Database Migration Service](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.ConnectionAttributes.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L193">property kmsKeyArn</a>
</h3>

```typescript
kmsKeyArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L197">property mongodbSettings</a>
</h3>

```typescript
mongodbSettings?: pulumi.Input<{ ... }>;
```


Settings for the source MongoDB endpoint. Available settings are `auth_type` (default: `PASSWORD`), `auth_mechanism` (default: `DEFAULT`), `nesting_level` (default: `NONE`), `extract_doc_id` (default: `false`), `docs_to_investigate` (default: `1000`) and `auth_source` (default: `admin`). For more details, see [Using MongoDB as a Source for AWS DMS](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.MongoDB.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L201">property password</a>
</h3>

```typescript
password?: pulumi.Input<string>;
```


The password to be used to login to the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L205">property port</a>
</h3>

```typescript
port?: pulumi.Input<number>;
```


The port used by the endpoint database.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L209">property s3Settings</a>
</h3>

```typescript
s3Settings?: pulumi.Input<{ ... }>;
```


Settings for the target S3 endpoint. Available settings are `service_access_role_arn`, `external_table_definition`, `csv_row_delimiter` (default: `\\n`), `csv_delimiter` (default: `,`), `bucket_folder`, `bucket_name` and `compression_type` (default: `NONE`). For more details, see [Using Amazon S3 as a Target for AWS Database Migration Service](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.S3.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L213">property serverName</a>
</h3>

```typescript
serverName?: pulumi.Input<string>;
```


The host name of the server.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L217">property serviceAccessRole</a>
</h3>

```typescript
serviceAccessRole?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) used by the service access IAM role for dynamodb endpoints.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L221">property sslMode</a>
</h3>

```typescript
sslMode?: pulumi.Input<string>;
```


The SSL mode to use for the connection. Can be one of `none | require | verify-ca | verify-full`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L225">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/endpoint.ts#L229">property username</a>
</h3>

```typescript
username?: pulumi.Input<string>;
```


The user name to be used to login to the endpoint database.

<h2 class="pdoc-module-header" id="ReplicationInstanceArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L229">interface ReplicationInstanceArgs</a>
</h2>

The set of arguments for constructing a ReplicationInstance resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L233">property allocatedStorage</a>
</h3>

```typescript
allocatedStorage?: pulumi.Input<number>;
```


The amount of storage (in gigabytes) to be initially allocated for the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L237">property applyImmediately</a>
</h3>

```typescript
applyImmediately?: pulumi.Input<boolean>;
```


Indicates whether the changes should be applied immediately or during the next maintenance window. Only used when updating an existing resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L241">property autoMinorVersionUpgrade</a>
</h3>

```typescript
autoMinorVersionUpgrade?: pulumi.Input<boolean>;
```


Indicates that minor engine upgrades will be applied automatically to the replication instance during the maintenance window.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L245">property availabilityZone</a>
</h3>

```typescript
availabilityZone?: pulumi.Input<string>;
```


The EC2 Availability Zone that the replication instance will be created in.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L249">property engineVersion</a>
</h3>

```typescript
engineVersion?: pulumi.Input<string>;
```


The engine version number of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L253">property kmsKeyArn</a>
</h3>

```typescript
kmsKeyArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L257">property multiAz</a>
</h3>

```typescript
multiAz?: pulumi.Input<boolean>;
```


Specifies if the replication instance is a multi-az deployment. You cannot set the `availability_zone` parameter if the `multi_az` parameter is set to `true`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L261">property preferredMaintenanceWindow</a>
</h3>

```typescript
preferredMaintenanceWindow?: pulumi.Input<string>;
```


The weekly time range during which system maintenance can occur, in Universal Coordinated Time (UTC).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L265">property publiclyAccessible</a>
</h3>

```typescript
publiclyAccessible?: pulumi.Input<boolean>;
```


Specifies the accessibility options for the replication instance. A value of true represents an instance with a public IP address. A value of false represents an instance with a private IP address.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L269">property replicationInstanceClass</a>
</h3>

```typescript
replicationInstanceClass: pulumi.Input<string>;
```


The compute and memory capacity of the replication instance as specified by the replication instance class. Can be one of `dms.t2.micro | dms.t2.small | dms.t2.medium | dms.t2.large | dms.c4.large | dms.c4.xlarge | dms.c4.2xlarge | dms.c4.4xlarge`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L273">property replicationInstanceId</a>
</h3>

```typescript
replicationInstanceId: pulumi.Input<string>;
```


The replication instance identifier. This parameter is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L277">property replicationSubnetGroupId</a>
</h3>

```typescript
replicationSubnetGroupId?: pulumi.Input<string>;
```


A subnet group to associate with the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L281">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L285">property vpcSecurityGroupIds</a>
</h3>

```typescript
vpcSecurityGroupIds?: pulumi.Input<pulumi.Input<string>[]>;
```


A list of VPC security group IDs to be used with the replication instance. The VPC security groups must work with the VPC containing the replication instance.

<h2 class="pdoc-module-header" id="ReplicationInstanceState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L155">interface ReplicationInstanceState</a>
</h2>

Input properties used for looking up and filtering ReplicationInstance resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L159">property allocatedStorage</a>
</h3>

```typescript
allocatedStorage?: pulumi.Input<number>;
```


The amount of storage (in gigabytes) to be initially allocated for the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L163">property applyImmediately</a>
</h3>

```typescript
applyImmediately?: pulumi.Input<boolean>;
```


Indicates whether the changes should be applied immediately or during the next maintenance window. Only used when updating an existing resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L167">property autoMinorVersionUpgrade</a>
</h3>

```typescript
autoMinorVersionUpgrade?: pulumi.Input<boolean>;
```


Indicates that minor engine upgrades will be applied automatically to the replication instance during the maintenance window.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L171">property availabilityZone</a>
</h3>

```typescript
availabilityZone?: pulumi.Input<string>;
```


The EC2 Availability Zone that the replication instance will be created in.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L175">property engineVersion</a>
</h3>

```typescript
engineVersion?: pulumi.Input<string>;
```


The engine version number of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L179">property kmsKeyArn</a>
</h3>

```typescript
kmsKeyArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the KMS key that will be used to encrypt the connection parameters. If you do not specify a value for `kms_key_arn`, then AWS DMS will use your default encryption key. AWS KMS creates the default encryption key for your AWS account. Your AWS account has a different default encryption key for each AWS region.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L183">property multiAz</a>
</h3>

```typescript
multiAz?: pulumi.Input<boolean>;
```


Specifies if the replication instance is a multi-az deployment. You cannot set the `availability_zone` parameter if the `multi_az` parameter is set to `true`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L187">property preferredMaintenanceWindow</a>
</h3>

```typescript
preferredMaintenanceWindow?: pulumi.Input<string>;
```


The weekly time range during which system maintenance can occur, in Universal Coordinated Time (UTC).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L191">property publiclyAccessible</a>
</h3>

```typescript
publiclyAccessible?: pulumi.Input<boolean>;
```


Specifies the accessibility options for the replication instance. A value of true represents an instance with a public IP address. A value of false represents an instance with a private IP address.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L195">property replicationInstanceArn</a>
</h3>

```typescript
replicationInstanceArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L199">property replicationInstanceClass</a>
</h3>

```typescript
replicationInstanceClass?: pulumi.Input<string>;
```


The compute and memory capacity of the replication instance as specified by the replication instance class. Can be one of `dms.t2.micro | dms.t2.small | dms.t2.medium | dms.t2.large | dms.c4.large | dms.c4.xlarge | dms.c4.2xlarge | dms.c4.4xlarge`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L203">property replicationInstanceId</a>
</h3>

```typescript
replicationInstanceId?: pulumi.Input<string>;
```


The replication instance identifier. This parameter is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L207">property replicationInstancePrivateIps</a>
</h3>

```typescript
replicationInstancePrivateIps?: pulumi.Input<pulumi.Input<string>[]>;
```


A list of the private IP addresses of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L211">property replicationInstancePublicIps</a>
</h3>

```typescript
replicationInstancePublicIps?: pulumi.Input<pulumi.Input<string>[]>;
```


A list of the public IP addresses of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L215">property replicationSubnetGroupId</a>
</h3>

```typescript
replicationSubnetGroupId?: pulumi.Input<string>;
```


A subnet group to associate with the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L219">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationInstance.ts#L223">property vpcSecurityGroupIds</a>
</h3>

```typescript
vpcSecurityGroupIds?: pulumi.Input<pulumi.Input<string>[]>;
```


A list of VPC security group IDs to be used with the replication instance. The VPC security groups must work with the VPC containing the replication instance.

<h2 class="pdoc-module-header" id="ReplicationSubnetGroupArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L116">interface ReplicationSubnetGroupArgs</a>
</h2>

The set of arguments for constructing a ReplicationSubnetGroup resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L120">property replicationSubnetGroupDescription</a>
</h3>

```typescript
replicationSubnetGroupDescription: pulumi.Input<string>;
```


The description for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L124">property replicationSubnetGroupId</a>
</h3>

```typescript
replicationSubnetGroupId: pulumi.Input<string>;
```


The name for the replication subnet group. This value is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L128">property subnetIds</a>
</h3>

```typescript
subnetIds: pulumi.Input<pulumi.Input<string>[]>;
```


A list of the EC2 subnet IDs for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L132">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h2 class="pdoc-module-header" id="ReplicationSubnetGroupState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L89">interface ReplicationSubnetGroupState</a>
</h2>

Input properties used for looking up and filtering ReplicationSubnetGroup resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L90">property replicationSubnetGroupArn</a>
</h3>

```typescript
replicationSubnetGroupArn?: pulumi.Input<string>;
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L94">property replicationSubnetGroupDescription</a>
</h3>

```typescript
replicationSubnetGroupDescription?: pulumi.Input<string>;
```


The description for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L98">property replicationSubnetGroupId</a>
</h3>

```typescript
replicationSubnetGroupId?: pulumi.Input<string>;
```


The name for the replication subnet group. This value is stored as a lowercase string.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L102">property subnetIds</a>
</h3>

```typescript
subnetIds?: pulumi.Input<pulumi.Input<string>[]>;
```


A list of the EC2 subnet IDs for the subnet group.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L106">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationSubnetGroup.ts#L110">property vpcId</a>
</h3>

```typescript
vpcId?: pulumi.Input<string>;
```


The ID of the VPC the subnet group is in.

<h2 class="pdoc-module-header" id="ReplicationTaskArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L171">interface ReplicationTaskArgs</a>
</h2>

The set of arguments for constructing a ReplicationTask resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L175">property cdcStartTime</a>
</h3>

```typescript
cdcStartTime?: pulumi.Input<string>;
```


The Unix timestamp integer for the start of the Change Data Capture (CDC) operation.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L179">property migrationType</a>
</h3>

```typescript
migrationType: pulumi.Input<string>;
```


The migration type. Can be one of `full-load | cdc | full-load-and-cdc`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L183">property replicationInstanceArn</a>
</h3>

```typescript
replicationInstanceArn: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L187">property replicationTaskId</a>
</h3>

```typescript
replicationTaskId: pulumi.Input<string>;
```


The replication task identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L191">property replicationTaskSettings</a>
</h3>

```typescript
replicationTaskSettings?: pulumi.Input<string>;
```


An escaped JSON string that contains the task settings. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L195">property sourceEndpointArn</a>
</h3>

```typescript
sourceEndpointArn: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the source endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L199">property tableMappings</a>
</h3>

```typescript
tableMappings: pulumi.Input<string>;
```


An escaped JSON string that contains the table mappings. For information on table mapping see [Using Table Mapping with an AWS Database Migration Service Task to Select and Filter Data](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TableMapping.html)

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L203">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L207">property targetEndpointArn</a>
</h3>

```typescript
targetEndpointArn: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the target endpoint.

<h2 class="pdoc-module-header" id="ReplicationTaskState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L125">interface ReplicationTaskState</a>
</h2>

Input properties used for looking up and filtering ReplicationTask resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L129">property cdcStartTime</a>
</h3>

```typescript
cdcStartTime?: pulumi.Input<string>;
```


The Unix timestamp integer for the start of the Change Data Capture (CDC) operation.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L133">property migrationType</a>
</h3>

```typescript
migrationType?: pulumi.Input<string>;
```


The migration type. Can be one of `full-load | cdc | full-load-and-cdc`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L137">property replicationInstanceArn</a>
</h3>

```typescript
replicationInstanceArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) of the replication instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L141">property replicationTaskArn</a>
</h3>

```typescript
replicationTaskArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) for the replication task.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L145">property replicationTaskId</a>
</h3>

```typescript
replicationTaskId?: pulumi.Input<string>;
```


The replication task identifier.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L149">property replicationTaskSettings</a>
</h3>

```typescript
replicationTaskSettings?: pulumi.Input<string>;
```


An escaped JSON string that contains the task settings. For a complete list of task settings, see [Task Settings for AWS Database Migration Service Tasks](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TaskSettings.html).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L153">property sourceEndpointArn</a>
</h3>

```typescript
sourceEndpointArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the source endpoint.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L157">property tableMappings</a>
</h3>

```typescript
tableMappings?: pulumi.Input<string>;
```


An escaped JSON string that contains the table mappings. For information on table mapping see [Using Table Mapping with an AWS Database Migration Service Task to Select and Filter Data](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Tasks.CustomizingTasks.TableMapping.html)

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L161">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/dms/replicationTask.ts#L165">property targetEndpointArn</a>
</h3>

```typescript
targetEndpointArn?: pulumi.Input<string>;
```


The Amazon Resource Name (ARN) string that uniquely identifies the target endpoint.

