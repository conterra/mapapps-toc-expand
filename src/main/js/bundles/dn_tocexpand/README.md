# dn_tocexpand

The Toc Expand bundle allows you to expand groups in the toc at startup.

## Usage
**Requirement: map.apps 4.7.0**

1. First you need to add the bundle dn_tocexpand to your app.
2. Then you can expand every map content by adding the _expanded_ property to a layer.

```javascript
"map": {
    "layers": [
        {
            "id": "koeln2",
            "title": "${map.koeln2.title}",
            "description": "${map.koeln2.description}",
            "type": "GROUP",
            "expanded": true,
            "layers": [
                {
                    "title": "${map.koeln2.libraries.title}",
                    "url": "https://services.arcgis.com/ObdAEOfl1Z5LP2D0/arcgis/rest/services/Köln/FeatureServer/1",
                    "type": "AGS_FEATURE",
                    "visible": true,
                    "popupTemplate": {
                        "title": "{NAME_LANG}",
                        "content": [
                            {
                                "type": "fields",
                                "fieldInfos": [
                                    {
                                        "fieldName": "NAME_LANG",
                                        "label": "${common.name}"
                                    },
                                    {
                                        "fieldName": "ADRESSE",
                                        "label": "${common.address}"
                                    },
                                    {
                                        "fieldName": "PLZ",
                                        "label": "${common.zip}"
                                    }
                                ]
                            }
                        ]
                    }
                },
                ...
            ]
        }
    ]
}
```
