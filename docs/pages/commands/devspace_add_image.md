---
title: "Command - devspace add image"
sidebar_label: devspace add image
---


Add an image

## Synopsis

 
```
devspace add image [flags]
```

```
#######################################################
############# devspace add image ######################
#######################################################
Adds a new image to this project's devspace.yaml

Examples:
devspace add image my-image --image=dockeruser/devspaceimage2
devspace add image my-image --image=dockeruser/devspaceimage2 --tag=alpine
devspace add image my-image --image=dockeruser/devspaceimage2 --context=./context
devspace add image my-image --image=dockeruser/devspaceimage2 --dockerfile=./Dockerfile
devspace add image my-image --image=dockeruser/devspaceimage2 --buildtool=docker
devspace add image my-image --image=dockeruser/devspaceimage2 --buildtool=kaniko
#######################################################
```


## Flags

```
      --buildtool string    Specify which engine should build the file. Should match this regex: docker|kaniko
      --context string      The path of the images' context
      --dockerfile string   The path of the images' dockerfile
  -h, --help                help for image
      --image string        The image name of the image (e.g. myusername/devspace)
      --tag string          The tag of the image
```


## Global & Inherited Flags

```
      --config string            The devspace config file to use
      --debug                    Prints the stack trace if an error occurs
      --inactivity-timeout int   Minutes the current user is inactive (no mouse or keyboard interaction) until DevSpace will exit automatically. 0 to disable (default 180)
      --kube-context string      The kubernetes context to use
  -n, --namespace string         The kubernetes namespace to use
      --no-warn                  If true does not show any warning when deploying into a different namespace or kube-context than before
  -p, --profile string           The devspace profile to use (if there is any)
      --profile-parent strings   One or more profiles that should be applied before the specified profile (e.g. devspace dev --profile-parent=base1 --profile-parent=base2 --profile=my-profile)
      --profile-refresh          If true will pull and re-download profile parent sources
      --restore-vars             If true will restore the variables from kubernetes before loading the config
      --save-vars                If true will save the variables to kubernetes after loading the config
      --silent                   Run in silent mode and prevents any devspace log output except panics & fatals
  -s, --switch-context           Switches and uses the last kube context and namespace that was used to deploy the DevSpace project
      --var strings              Variables to override during execution (e.g. --var=MYVAR=MYVALUE)
      --vars-secret string       The secret to restore/save the variables from/to, if --restore-vars or --save-vars is enabled (default "devspace-vars")
```

