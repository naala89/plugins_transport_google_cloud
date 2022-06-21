# Transport Google Cloud

Transport for ApiOpenStudio output to Google Cloud.

# Adding to your project

## Composer

    $ composer require apiopenstudio/transport_google_cloud

# Configuration

Add a remote output processor to your resource.

The output section example below will return the output in the response as well
as upload the response to a Google Cloud server:

    output:
        -
            processor: json_remote
            id: example JSON Remote output
            filename: example.json
            transport: ApiOpenStudio\Plugins\TransportGoogleCloud
            parameters:
                bucket: my_google_cloud_bucket
                prefix: my_google_cloud_prefix (optional)
        - 
            response

**Note:** the value for the transport is the full namespace path.

## Parameters

### Required

- key - AWS S3 key
- secret - AWS S3 secret
- bucket - AWS S3 bucket name
- version - latest|version

### Optional

- region - AWS S3 bucket region

# Further information

See [FlySystem documentation][flysystem-docs] and
[The League GitHub][flysystem-github] for more details.

[flysystem-github]: https://github.com/thephpleague/flysystem-google-cloud-storage

[flysystem-docs]: https://flysystem.thephpleague.com/docs/adapter/google-cloud-storage/
