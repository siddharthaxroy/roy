# Roy Lab website — how to update

Built with Hugo and deployed by Netlify on every push to `master`.

## Where things live

| To change…                    | Edit this                                   |
|-------------------------------|---------------------------------------------|
| News                          | `content/news/index.md` (pictures in the same folder) |
| Publications                  | `data/publications.yaml`                    |
| Op-eds / essays (Outreach)    | `data/essays.yaml`                          |
| Lab members and alumni        | `data/people.yaml` (photos in `content/people/`) |
| Text of any page              | `content/<page>/index.md`                   |
| Home page text                | `content/_index.md`                         |
| Home-page slideshow           | add/remove `static/img/carousel-*.jpg`      |
| Menu, address, social links   | `config.toml`                               |
| Colors and fonts              | `static/css/site.css`                       |

## Adding a news item

Open `content/news/index.md`, copy an existing block, paste it under the right year and edit it:

```
{{< news date="January 15, 2026" image="26-01-schools.jpg" >}}
### New paper on lead in schools

One or two sentences about it. [Read the paper ↗](https://doi.org/...)
{{< /news >}}
```

Upload the picture to `content/news/`. No picture? Leave out `image=...` (an icon shows instead), or pick one with `icon="🎤"`.

## Shortcodes you can use inside page text

- `{{< youtube VIDEO_ID >}}` — embedded YouTube video
- `{{< tweet TWEET_ID >}}` — link to a tweet (no live embed, so builds never depend on Twitter)
- `{{< figure src="/img/photo.jpg" caption="..." position="center" >}}` — image with caption
- `{{< image src="/img/photo.jpg" position="center" >}}` — plain image

## Preview locally (optional)

Install Hugo 0.74.3 extended, then run `hugo server` in this folder and open http://localhost:1313.
