# Wrike Activities
Wrike API v4 ( https://developers.wrike.com/documentation/api/overview ) のうち、UiPathでワークフローを作成するのに最低限必要なものだけ実装しています。認証はPermanent access token方式のみをサポートしていますので、App Consoleで、事前にPermanent access tokenを取得してください。

## 実装されているメソッド

### Get Tasks
Search among all tasks in the account
( https://developers.wrike.com/documentation/api/methods/query-tasks )

#### Input

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| AccessToken    | Permanent access token(必須) |

#### Output

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| Tasks          | Task List (DataTable) { id } |

### Get Task
Returns complete information about single task
( https://developers.wrike.com/documentation/api/methods/query-tasks )

#### Input

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| AccessToken    | Permanent access token(必須) |
| TaskId         | Task ID(必須)                |

#### Output

| パラメーター名 | 内容                |
|:---------------|:--------------------|
| Task           | Task Data (JObject) |

### Get Attachments
Returns all Attachments of a task
( https://developers.wrike.com/documentation/api/methods/get-attachments )

#### Input

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| AccessToken    | Permanent access token(必須) |
| TaskId         | Task ID(必須)                |

### Download Attachment
Download attachment content
( https://developers.wrike.com/documentation/api/methods/download-wrike-attachment )

#### Input

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| AccessToken    | Permanent access token(必須) |
| AttachmentId   | Attachment ID(必須)          |
| Name           | Download file name           |

### Create Comment
Create comment in task
( https://developers.wrike.com/documentation/api/methods/create-comment )

#### Input

| パラメーター名 | 内容                                                            |
|:---------------|:----------------------------------------------------------------|
| AccessToken    | Permanent access token(必須)                                    |
| TaskId         | Task ID(必須)                                                   |
| PlainText      | Treat comment text as plain text, HTML otherwise(Default False) |
| Text           | Comment text(必須)                                              |

### Modify Task

#### Input

| パラメーター名 | 内容                         |
|:---------------|:-----------------------------|
| AccessToken    | Permanent access token(必須) |
