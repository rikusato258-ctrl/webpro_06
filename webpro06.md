```mermaid
stateDiagram-v2
delate --> entry:削除処理
entry :  /keiyo2
entry --> /keiyo2/#58;number:詳細表示
 /keiyo2/#58;number --> entry:一覧表示

/keiyo2/#58;number --> /keiyo2/edit/#58number:編集
/keiyo2/edit/#58number --> entry:一覧表示
/keiyo2/edit/#58number --> /keiyo2/update/#58;number:一覧表示

/keiyo2/update/#58;number --> entry:一覧表示

register : /keiyo2/create
entry --> register:新規登録
register --> entry:一覧表示

new_register : post /keiyo2
register --> new_register:新規登録処理
new_register --> entry:一覧表示


```