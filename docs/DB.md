# Database entities
Note: all tables linked with association tables.

## binary_group
| col     | type | description       | example      |
|---------|------|-------------------|--------------|
| id      | int  | id                | 12345        |
| name    | str  | binary group name | log4j        |
| descr   | str  | description       | Apache Log4J |

## binary
| col       | type | description           | example            |
|-----------|------|-----------------------|--------------------|
| id        | int  | id                    | 12345              |
| name      | str  | binary name           | log4j-1.2.jar      |
| descr     | str  | description           | Log4J Java library |
| local_url | url  | local binary location | .../log4j-1.2.jar  |
| version   | str  | version               | 1.2                |
| type      | enum | jar, exec, ...        | jar                |
| license   | enum | Apache, GPLv3, ...    | jar                |
| created   | date | create date           | 2023-07-01         |
| updated   | date | update date           | 2023-08-01         |

## source
| col      | type | description   | example                                   |
|----------|------|---------------|-------------------------------------------|
| id       | int  | id            | 12345                                     |
| b_length | int  | binary length | 1024                                      |
| url      | str  | source url    | https://repo1.maven.org/.../log4j-1.2.jar |
| checked  | date | update date   | 2023-08-01                                |

## hash
| col      | type | description   | example |
|----------|------|---------------|---------|
| id       | int  | id            | 12345   |
| md5      | str  | MD5           | ...     |
| sha256   | str  | SHA256        | ...     |
