# studio
 
Library Eksperiment membuat mengedit video / audio / photo di server side & client side.

## List Menu
  - [Docs](#docs)
  - [Quickstart](#quickstart)

## Quickstart

<details open>
<summary>Code</summary>

```dart
// ignore_for_file: depend_on_referenced_packages
import 'package:flutter/material.dart';
import 'package:studio/studio.dart';
void main() {
  Map<String, dynamic> medias = {
      
  };
  runApp(Studio(medias));
}
``` 

</details>

## Docs
Basic membuat widget / applikasi adalah sebagai berikut
| key     |              value              | Deskripsi | `required` |
|---------|:-------------------------------:|:----------|:----------:|
| `@type` |        [Type Edit](#type-edit)        |           |   `yes`    |

Contoh
```json
{
    "@type": "video",
    "medias": [
        [
            {
                "@type": "video",
                "video": "/vide.mp4",
                "duration": 12345
            },
            {
                "@type": "video",
                "video": "/vide.mp4",
                "duration": 12345
            }
        ],
        [
            {
                "@type": "photo",
                "photo": "/photo.png",
                "duration": 12345
            }
        ]
    ],
    "audios": [
        {
            "@type": "audio",
            "path": "/song.mp3"
        }
    ]
}
```

## type edit

#### Audio
| key     |       value       | Deskripsi | `required` |
|---------|:-----------------:|:----------|:----------:|
| `@type` |    `audio`     |           |   `yes`    |
| `audios`  | [Audio](#audio) |           |   `yes`    |

#### Photo
| key     |       value       | Deskripsi | `required` |
|---------|:-----------------:|:----------|:----------:|
| `@type` |    `photo`     |           |   `yes`    |
| `medias`  | [Photo](#photo) |           |   `yes`    |

#### Video
| key     |       value       | Deskripsi | `required` |
|---------|:-----------------:|:----------|:----------:|
| `@type` |    `video`     |           |   `yes`    |
| `medias`  | [Widget](#methods) |           |   `yes`    |
| `audios`  | [Audio](#audio) |           |   `no`    |

## methods

#### Audio
| key     |       value       | Deskripsi | `required` |
|---------|:-----------------:|:----------|:----------:|
| `@type` |    `audio`    |           |   `yes`    |
| `audio` | String path |           |   `yes`    |

#### Photo
| key     |       value       | Deskripsi | `required` |
|---------|:-----------------:|:----------|:----------:|
| `@type` |    `photo`    |           |   `yes`    |
| `photo` | String path |           |   `yes`    |

#### Video
| key     | value  | Deskripsi | `required` |
|---------|:------:|:----------|:----------:|
| `@type` | `video` |           |   `yes`    |
| `video`  | string path |           |   `yes`    |
