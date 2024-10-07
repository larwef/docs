---
title: K3sのアンインストール
---

:::warning
K3sをアンインストールすると、ローカルクラスターのデータ、設定、およびすべてのスクリプトとCLIツールが削除されます。  
外部データストアからのデータや、外部Kubernetesストレージボリュームを使用してポッドによって作成されたデータは削除されません。
:::

インストールスクリプトを使用してK3sをインストールした場合、インストール中にK3sをアンインストールするためのスクリプトが生成されました。

アンインストール後にノードを既存のクラスターに再参加させる予定がある場合は、ノードのパスワードシークレットが削除されるように、クラスターからノードを削除することを忘れないでください。詳細については、[ノード登録](../architecture.md#how-agent-node-registration-works)のドキュメントを参照してください。

### サーバーのアンインストール
サーバーノードからK3sをアンインストールするには、次のコマンドを実行します:

```bash
/usr/local/bin/k3s-uninstall.sh
```

### エージェントのアンインストール
エージェントノードからK3sをアンインストールするには、次のコマンドを実行します:

```bash
/usr/local/bin/k3s-agent-uninstall.sh
```