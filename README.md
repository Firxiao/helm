# Kubernetes Helm Charts

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add oncloudops https://helm.oncloudops.com/

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  
You can then run `helm search repo oncloudops` to see the charts.

To install the aliyun-ddns chart:

    # config.yaml
    # 阿里云 Access Key ID
    access_key_id: "FFFFFFFFFF"
    # 阿里云 Access Key Secret
    access_key_secret: "FFFFFFFFFF"
    # 阿里云 一级域名
    rc_domain: "example.com"
    # 解析记录
    rc_rr_list: "foo,bar"

    helm install my-aliyun-ddns aliyun-ddns  -f config.yaml

To uninstall the chart:

    helm delete my-aliyun-ddns
