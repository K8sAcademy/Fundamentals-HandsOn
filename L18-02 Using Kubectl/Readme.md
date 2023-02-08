# L18-02

## Current context

Get the current context:

    kubectl config current-context

## List all contexts

List all the contexts:

    kubectl config get-contexts

## Change context

Use a context:

    kubectl config use-context [contextName]

## Using kubectx

What's great about Kubernetes is the incredible amount of tools created by the community and available for free.  Kubectx is a simple tool that provides an easy way to list and change context.

You can install it on:

Windows (if you have Chocolatey installed):

    choco install kubectx-ps

macOS (if you have Brew installed):

    brew install kubectx

Ubuntu:

    sudo apt install kubectx

To list the contexts, simply type:

    kubectx

To change context:

    kubectx <contextName>

## Rename context

Rename context:

    kubectl config rename-context [old-name] [new-name]

## Delete context

Delete context:

    kubectl config delete-context [contextName]