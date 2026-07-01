[leafletjs-playground](https://dirkarnez.github.io/leafletjs-playground)
========================================================================
### Tutorials
- [Leaflet Playground](https://codepen.io/njosefbeck/pen/EZaEbj)
- [Leaflet on Mobile](https://leafletjs.com/examples/mobile)

### TODOs
- [ ] GPS web api
- [ ] precache (PWA)
  - https://github.com/reyemtm/pwa-maps
  - ```js
    // 在 service-worker.js 中
    import { precacheAndRoute } from 'workbox-precaching';
    import { registerRoute } from 'workbox-routing';
    import { StaleWhileRevalidate, CacheFirst } from 'workbox-strategies';
    
    // 1. 預快取應用程式框架 (HTML, CSS, JS)
    precacheAndRoute(self.__WB_MANIFEST);
    
    // 2. 快取 OpenStreetMap 圖磚 (動態 Runtime 策略)
    registerRoute(
      ({ url }) => url.origin === 'https://tile.openstreetmap.org',
      new StaleWhileRevalidate({
        cacheName: 'osm-tiles',
        plugins: [
          {
            cacheableResponse: { statuses: [0, 200] }
          }
        ]
      })
    );
    ```
- [ ] Offline routers
  - https://wiki.openstreetmap.org/wiki/Routing
  - https://wiki.openstreetmap.org/wiki/Routing/offline_routers
### Data sources
- [Home | DATA.GOV.HK](https://data.gov.hk/en/)
- [Home - LANDSD MAP API PORTAL for Government Bureaux / Departments](https://api.portal.hkmapservice.gov.hk/)
- [Map APIs](https://portal.csdi.gov.hk/csdi-webpage/apilist)
