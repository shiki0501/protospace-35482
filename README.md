
## usersテーブル
| column     | type   | options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association
- has_many :prototype
- has_many :comment

## prototypeテーブル
| column      | type           | options     |
| ----------- | -------------- | ----------- |
| title       | string         | null: false |
| catch_copy  | text           | null: false |
| concept     | text           | null: false |
| image       |                |             |
| user        | references     |             |

### Association
- has_many :comment
- belongs_to :user

## commentsテーブル
| column    | type       | option      |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             |
| prototype | references |             |

### Association
- belongs_to :user
- belongs_to :prototype