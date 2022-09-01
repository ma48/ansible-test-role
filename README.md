# ansible-test-role

検証利用のためのAnsible Role。
httpdをインストールしてlocalhost.confとindex.htmlを作成している。

## 利用想定

`ansible-galaxy install`を利用して任意のrolesディレクトリへダウンロードして利用する

```sh
$ ansible-galaxy install -r requirements.yml --roles-path /your/roles/path
Starting galaxy role install process
- extracting test-httpd to /your/roles/path/roles/test-httpd
- test-httpd (v0.1.0) was installed successfully
[WARNING]: Meta file /your/roles/path/test-httpd is empty. Skipping dependencies.
```

### requirements.ymlの具体例

※参考
[Installing Multiple Roles From a File](https://galaxy.ansible.com/docs/using/installing.html#installing-multiple-roles-from-a-file)

```yaml
# https://galaxy.ansible.com/docs/using/installing.html#installing-multiple-roles-from-a-file
# from github
- src: git@github.com:{GitHub組織名}/ansible-test-role.git
  scm: git
  version: v0.1.0
  name: test-httpd

# from galaxy
- src: yatesr.timezone

# from GitHub
- src: https://github.com/bennojoy/nginx
```

## Licence

MIT
