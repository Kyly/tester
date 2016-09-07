
**LS iFrame Events API**
- **API**

  | Event                | Type                             | Payload         | Description                             |  
  |----------------------|----------------------------------|-----------------|-----------------------------------------|  
  | ls.alert.event       | (danger\|success\|warning\|info) | shown below     | Messages to be displayed to end user    |  
  | ls.onLoad.event      | loaded                           | none            | Indicates when frames content is loaded | 

- **Payload**
  ```
  {
    type: (danger|success|warning|info),
    title: string,
    message: string
  }
  ```


**Performance**
Intellect follows _RAIL Performance Model_ as a guideline to measure our UI.
Details can be found [here](https://developers.google.com/web/tools/chrome-devtools/profile/evaluate-performance/rail).

| RAIL Step | Key Metric	                                                    | User Actions |
|-----------|-----------------------------------------------------------------|--------------|
| Response	| Input latency (from tap to paint) < 100ms.	                    | User taps on an icon or button (e.g., opening the nav menu, tapping Compose). |
| Response	| Input latency (from tap to paint) < 16ms.	                      | User drags their finger and the app's response is bound to the finger position | (e.g., pull to refresh, swiping a carousel). |
| Animation	| Input latency (from tap to paint) < 100ms for initial response.	| User initiates page scroll or animation begins. |
| Animation	| Each frame's work (JS to paint) completes < 16ms.	              | User scrolls the page or sees an animation. |
| Idle	    | Main thread JS work chunked no larger than 50ms.	              | User isn't interacting with the page, but main thread should be available enough | to handle the next user input. |
| Load	    | Page considered ready to use in 1000ms.	                        | User loads the page and sees the critical path content. |
| Load	    | Satisfy the Response goals during the full page load process.	  | User loads the page and starts interacting (e.g., scrolls or opens navigation). |

**CDN Packages** 

| Package   | Version    | Source                                                                     |  
|-----------|------------|----------------------------------------------------------------------------|  
| jQuery    | 1.11.1     | https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.4/jquery-ui.min.js |  
| Bootstrap | 3.3.6      | https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.6/js/bootstrap.min.js https://cdnjs.cloudflare.com/ajax/libs/classie/1.0.1/classie.min.js |  
| Lodash    | 4.14.2     | https://cdn.jsdelivr.net/lodash/4.14.2/lodash.min.js                       |  
