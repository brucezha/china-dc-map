# China Data Center Intelligence

Live map of 843+ data center facilities across China, combining Baxtel, datacenters.com, and AI-monitored news.

## Deployment (GitHub Pages)

1. Push this folder's contents to a GitHub repo (e.g. `china-dc-intelligence`)
2. Go to **Settings → Pages → Source → main branch / root**
3. Your map will be live at `https://yourusername.github.io/china-dc-intelligence`

## Updating News

Edit the `NEWS` array in `index.html` (search for `const NEWS = [`).  
Each entry follows this format:

```js
{
  id: 'news-006',
  date: '2026-04-01',
  headline: 'Headline here',
  summary: 'Brief description...',
  source: 'Source name',
  url: 'https://...',
  type: 'new_build', // new_build | expansion | acquisition | policy | announcement
  tags: ['Operator', 'Province'],
  dc_name: '',  // exact name of existing site if known (links news to marker)
  lat: null, lng: null  // coordinates if a new site
}
```

## Data Structure

Each site in `const DATA` has: `lat, lng, name, operator, city, province, stage, mw, pue, popup, prov_color, marker_color`

## Adding a New Site

Append to `const DATA`:
```js
{"lat":31.23,"lng":121.47,"name":"New Facility Name","operator":"Operator","city":"Shanghai","province":"Shanghai","stage":"construction","mw":"100","pue":"","popup":"<b>New Facility</b>...","chip":"","prov_color":"#3cb44b","marker_color":"#f0883e"}
```
