# want-to-build
> :scroll: List of projects that I want to build

This is a common problem that I come up with some cool ideas, but don't have time to build them. But when I finally have some time or my friend/colleague asks for some idea she can build I can't think of any of the top of my head 😭

To solve this I'll keep the list of my ideas and small descriptions of them here.

## Not started

This are the projects I haven't started working on

### EZlytics

Self-hosted analytics with server-side and simle client code and nice admin ui. 

 - should allow to track pageviews and custom events (like `ga('send', 'pageview', location.pathname);`)
 - combine events into sessions 
 - have a nice viewer for sessions
 
### YZtesting

Self-hosted AB-testing tool, that cares about your conversion. Most of the A/B testing tools(Optimizely, VWO) are really bloated and hard to use. But from developers point of view you just need to know a test you're running and what variation to show. Also without proper setup they can kill your conversions by leading to a losing variation.

Example React pseudocode:

```jsx
const test = YZ.getTest('123');
const variation = test.variation; // Can contain some data, or just a `variation.id` can be used to decide what to render

render() {
  return (
   <button 
     onClick={()=>{
       // do some real stuff
       test.reportSuccess(); // test knows what variation was used
     }}
   >
     {variation.text}
   </button>
  );
}

```

