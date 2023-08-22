# CKAN Cloudstorage API

<div align="center">
  <em>Extension to manage CKAN resources in any S3-like object storage.</em>
</div>
<div align="center">
  <a href="https://pypi.org/project/ckanext-cloudstorage_api" target="_blank">
      <img src="https://img.shields.io/pypi/v/ckanext-cloudstorage_api?color=%2334D058&label=pypi%20package" alt="Package version">
  </a>
  <a href="https://pypistats.org/packages/ckanext-cloudstorage_api" target="_blank">
      <img src="https://img.shields.io/pypi/dm/ckanext-cloudstorage_api.svg" alt="Downloads">
  </a>
  <a href="https://gitlabext.wsl.ch/EnviDat/ckanext-cloudstorage_api/-/raw/main/LICENSE" target="_blank">
      <img src="https://img.shields.io/github/license/EnviDat/ckanext-cloudstorage_api.svg" alt="Licence">
  </a>
</div>

---

**Documentation**: <a href="https://envidat.gitlab-pages.wsl.ch/ckanext-cloudstorage_api/" target="_blank">https://envidat.gitlab-pages.wsl.ch/ckanext-cloudstorage_api/</a>

**Source Code**: <a href="https://gitlabext.wsl.ch/EnviDat/ckanext-cloudstorage_api" target="_blank">https://gitlabext.wsl.ch/EnviDat/ckanext-cloudstorage_api</a>

---

**This plugin is primarily intended for custom frontends built on the CKAN API.**

Supports any S3-like API, e.g. Minio, Ceph Object Gateway.

Full support for all Apache libcloud drivers was dropped, due to primarily relying on S3 multipart and pre-signed URL capabilities.

## Install

```bash
pip install ckanext-cloudstorage-api
```

## Config

Required variables are set in your ckan.ini:

- **ckanext.cloudstorage_api.host**
  - Description: The S3 host URL.
- **ckanext.cloudstorage_api.region**
  - Description: The S3 host region.
- **ckanext.cloudstorage_api.access_key**
  - Description: Access key for S3.
- **ckanext.cloudstorage_api.secret_key**
  - Description: Secret key for S3.
- **ckanext.cloudstorage_api.bucket_name**
  - Description: The name of the S3 bucket to store files.
- **ckanext.cloudstorage_api.max_multipart_lifetime**
  - Description: (Optional) maximum time a multipart part can exist.
    Multiparts will be cleaned if older than this by
    calling the cloudstorage_clean_multiparts endpoint.

## Endpoints

TBC
