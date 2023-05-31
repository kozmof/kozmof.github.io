---
title: 3Dモデルを表示できるようにした
date: 2023-05-16
draft: false
tags: ['hugo', 'design']
---

Sketchfab経由などではなく、ブログにモデルを直接表示する機能があるのを見たことがないなとふと思い、モデルの表示機能を[作った](https://github.com/kozmof/archie/blob/master/layouts/shortcodes/model.html)。
                                                                  

[model-viewer](https://github.com/google/model-viewer)を使用し、下記のようにパスを指定すれば表示できる。

```markdown
{{</*
    model
    alt="Scotch Boiler from PS Waverley by Scottish Maritime Museum"
    src="model/scotch_boiler_from_ps_waverley_1k.glb"
*/>}}
```

{{<
    model
    alt="Scotch Boiler from PS Waverley by Scottish Maritime Museum"
    src="model/scotch_boiler_from_ps_waverley_1k.glb"
>}}
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

[Scotch Boiler from "PS Waverley"](https://sketchfab.com/3d-models/scotch-boiler-from-ps-waverley-88fdf5e81ff64885b2ce2ea9e0a9aede) by Scottish Maritime Museum 

{{<
    model
    alt="Air – Sea Rescue Craft (ASR-10) by Scottish Maritime Museum"
    src="model/air__sea_rescue_craft_asr-10_1k.glb"
>}}

[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)

[Air – Sea Rescue Craft (ASR-10)]( https://sketchfab.com/3d-models/air-sea-rescue-craft-asr-10-7f54d6af39674fb88f43bd48af3944c5) by Scottish Maritime Museum
