# jenkins

This pack contains all you need to deploy jenkins (version 2 by default) in Nomad. It uses Docker driver.


## Variables

- `job_name` (string) - The name to use as the job name which overrides using the pack name.
- `region` (string) - The region where jobs will be deployed.
- `datacenters` (list of strings) - A list of datacenters in the region which are eligible for task placement.
- `namespace` (string) - The namespace where the job should be placed.
- `constraints` (string) - Constraints to apply to the entire job.
- `image_name` (string) - The docker image name.
- `image_tag` (string) - The docker image tag.
- `task_resources` (object, number number) Resources used by Jenkins task
- `register_consul_service` (bool) - If you want to register a consul service for the job
- `consul_service_name` (string) - The consul service name for the hello-world application
- `consul_service_tags` (list of string) - The consul service name for the hello-world application
- `volume_name` (string) - The name of the volume you want Jenkins to use
- `volume_type` (string) - The type of the volume you want Jenkins to use
- `docker_jenkins_env_vars` (map of string) - Environment variables to pass to Docker container

## Jenkins Environment Variables

You can pass the right environment variables to Jenkins.
An example of the `docker_jenkins_env_vars` to use is in the `vars.nomad` file.
