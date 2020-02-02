# Kubernetes で実践するクラウドネイティブ DevOps

![Kubernetes で実践するクラウドネイティブ DevOps の表紙](/img/cover-ja.jpg)

ようこそ！このリポジトリは、オライリー・ジャパン「Kubernetes で実践するクラウドネイティブ DevOps」に付属するサンプルコードです。原著である「Cloud Native DevOps with Kubernetes」が提供するサンプルコードから2019年10月時点で最新バージョンの Kubernetes 1.16 で動作するように修正しています。

本書の購入はこちらから:

* [アマゾン](https://www.amazon.co.jp/dp/4873119014/)

* [O'Reilly Japan](https://www.oreilly.co.jp/books/9784873119014/)

## 環境

サンプルコードのビルドと実行には次が必要です。

* Go バージョン 1.11 またはそれ以上
* Docker バージョン 18.3 またはそれ以上

## Kubernetes クラスタの構築

サンプルの設定ファイルは、Kubernetes 1.16 で動作を確認しています。ローカル環境に Kubernetes クラスタを構築するには Minikube または Kind、Docker Desktop が使用できます。Docker Desktop のセットアップ手順は本書に記載がありますのでご参照ください。

ここでは、Minikube と Kind で Kubernetes 1.16 のクラスタを作成する方法を説明します。

### Minikube

Minikube のインストールは「[Minikube のインストール](https://kubernetes.io/ja/docs/tasks/tools/install-minikube/)」にしたがってください。
```
minikube start --kubernetes-version=v1.16.4
```

### Kind

Kind のインストールは「[Quick Start](https://kind.sigs.k8s.io/docs/user/quick-start/)」にしたがってください。

```
kind create cluster --image=kindest/node:1.16.4
```

## オリジナルコード

サンプルコードのオリジナルは、 https://github.com/cloudnativedevops/demo です。

---

# Cloud Native DevOps with Kubernetes

![Cloud Native DevOps cover image](/img/cover.jpg)

Welcome! This is the example code repository to accompany the book 'Cloud Native DevOps with Kubernetes', by John Arundel and Justin Domingus. Buy the book here:

* [Amazon US](https://amzn.to/2PEPTjc)

* [Amazon UK](https://amzn.to/2PGkZa0)

* [O'Reilly](http://shop.oreilly.com/product/0636920175131.do)

## About the book

From the preface:

> You'll learn what Kubernetes is, where it comes from, and what it means for the future of software development and operations. You'll learn how containers work, how to build and manage them, and how to design cloud native services and infrastructure.

> You'll understand the trade-offs between building and hosting Kubernetes clusters yourself, and using managed services. You'll learn the capabilities, limitations, and pros and cons of popular Kubernetes installation tools such as kops, `kubeadm`, and Kubespray. You'll get an informed overview of the major managed Kubernetes offerings from the likes of Amazon, Google, and Microsoft.

> You'll get hands-on practical experience of writing and deploying Kubernetes applications, configuring and operating Kubernetes clusters, and automating cloud infrastructure and deployments with tools such as Helm. You'll learn about Kubernetes support for security, authentication, and permissions, including Role-Based Access Control (RBAC), and best practices for securing containers and Kubernetes in production.

> You'll learn how to set up continuous integration and deployment with Kubernetes, how to back up and restore data, how to test your cluster for conformance and reliability, how to monitor, trace, log, and aggregate metrics, and how to make your Kubernetes infrastructure scalable, resilient, and cost-effective.

The book aims to teach you everything you need to know to deploy, run, and scale applications in Kubernetes, and most importantly, to give you working example code for everything we demonstrate. That code is open source, available for free for you to use and adapt whether or not you buy the book. And here it is!

## Show me the code

Almost all the example code involves our 'hello world' demo application. Here is the list of examples; follow the links to see the documentation on each example.

* [Build and run the demo application locally](/hello) (start here!)
* [Deploy the app to Kubernetes using kubectl](/hello-k8s)
* [Deploy the app with Helm](/hello-helm)
* [Manage the app with Helmfile](/hello-helmfile)
* [Set up a namespace, resource requests, and limits for the app](/hello-namespace)
* [Add config data to the app's environment](/hello-config-env)
* [Pass config data to the app's command line](/hello-config-args)
* [Mount a config file in the container at runtime](/hello-config-file)
* [Add secret data to the app's environment](/hello-secret-env)
* [Mount a secrets file in the container](/hello-secret-file)
* [Store encrypted secrets in the app repo, decrypted automatically on deploy](/hello-sops)
* [Develop the app locally with Skaffold](/hello-skaffold)
* [Build and deploy the app automatically with Drone](/hello-drone)
* [Build and deploy the app automatically with Google Cloud Build](/hello-cloudbuild)

## Terraform examples

We also include some Terraform code examples, to help you manage cloud resources with code. Unfortunately we didn't have space to discuss these in the book, but we hope they'll be useful to you anyway.

### Google Cloud

* [Create a cloud storage bucket in code](/terraform/gcp/bucket)
* [Create a cloud database instance in code](/terraform/gcp/database)
* [Create a Kubernetes cluster in code](/terraform/gcp/k8scluster)

### Amazon AWS

* [Create a cloud storage bucket in code](/terraform/aws/bucket)
* [Create a cloud database instance in code](/terraform/aws/database)
* [Create a cloud virtual machine instance in code](/terraform/aws/vm)

## You will need

To build and run all of these examples, you will need:

* Go version 1.11 or above
* Docker version 18.03 or above

Where you need other tools for specific examples, we'll mention that in the README for the example.

## Contributing to the repo

We would absolutely love it if you contributed! Feel free to send us a PR to add new examples, add versions of the examples for different cloud providers (for example Microsoft Azure), or fix or improve the existing examples.
