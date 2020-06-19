# want-to-build
> :scroll: List of projects that I want to build

This is a common problem that I come up with some cool ideas, but don't have time to build them. But when I finally have some time or my friend/colleague asks for some ideas she can build I can't think of any of the top of my head 😭

To solve this I'll keep the list of my ideas and small descriptions of them here.

## Not started

These are the projects I haven't started working on

### YZtesting

Self-hosted AB-testing tool, that cares about your conversion. Most of the A/B testing tools(Optimizely, VWO) are really bloated and hard to use. But from developers point of view you just need to know a test you're running and what variation to show. Also, without proper setup they can kill your conversions by leading to a losing variation.

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

### KARMA inc.

Public database of Corporations misdeeds (and virtues).

A lot of big companies were caught doing some shady business([panama papers](http://panamapapers.sueddeutsche.de/en/), [paradise papers](https://www.icij.org/investigations/paradise-papers/), etc.) but it's quite hard to track what companies were actually involved and how bad it was. This database will aggregate all news articles about big companies(and maybe famous people) and provide overall `KARMA` score.

### Never Again

Social network/notebook for things that you don't want to do again(your fuckups or unpleasant experiences).

This is basically the opposite of life hacking. Stories can be saved privately, shared with your friends, or with everyone.

### rater

Create lists of things(food, places, artists, whatever) and tell what your rating scale is. Is it from 1 to 5 from 0 to 10? Maybe `x` to `y`? Is it ⭐️, 👍, `%` or ❤️ or maybe 💩?

List can be private or public, so you can share it with the world.

### Decentralized chat

> Inspired by [Gossip protocol](https://en.wikipedia.org/wiki/Gossip_protocol) and [Scuttlebutt](https://github.com/ssbc)

Chat where each client is also a server.

 - No centralized servers
 - First device you start using it with is a "master" by default
 - New devices ask master for permissions to access logs/history and to act on your behalf
 - Master can promote other devices to master level(so ideally you should have at least 2 masters in case of device loss, etc.)
 - Every message is encrypted
 - Offline delivery (in case recipient is offline) can be done through friends of friends or exchange hubs
 - 2 types of non-human servers (can be combined):
   - Exchange hubs: to simplify offline message delivery
   - Discovery hubs: to simplify user search
   
*NOTE:* [Berty](https://berty.tech) seems to be what I want.

### Emoji facemash
Facemash for emojis, to find emoji number 1! Also, comparing same emoji between different providers (google/apple) etc...

### News timeline aggregator
Service to link news(events) that happened at different times, but share same situation, actors, companies, etc.
This can be helpful to follow up on events(e.g. you know about Equifax fiasco, but don't know how the way situation developed, how it started and what were the latest news)

Similar to [timeline](https://itunes.apple.com/us/app/timeline-news-in-context/id948867534)


## Started

These are the projects that I've started but haven't finished

### To remember

Everyday photo diary. Works for just one(but very important) person right now.

### Sneak peek

App where you can exchange photos with a stranger. You can keep this photo dialogue until somebody stops to reply.

### [Macaque](https://github.com/phil-r/macaque)
> also known as `lodhommey`

Website crawler that uses a headless browser and finds errors and broken links on your website and reports it to you.

### [readhacker.news](https://readhacker.news/) email subscription

Allow [hackernewsbot](https://github.com/phil-r/hackernewsbot) to handle email subscriptions.

### [EZlytics](https://github.com/phil-r/ezlytics)

Self-hosted analytics with server-side and simple client code and nice admin ui.

 - should allow to track pageviews and custom events (like `ga('send', 'pageview', location.pathname);`)
 - combine events into sessions
 - have a nice viewer for sessions

Similar projects:

 - [PostHog](https://github.com/PostHog/posthog)

## Graveyard

These are the projects that I've wanted to build, but I won't for different reasons

### Temporary file-sharing service

> Inspired by [Firefox Send](https://github.com/mozilla/send)

Simple service to share files for the given amount of time or downloads, using [Backblaze B2](https://www.backblaze.com/b2/cloud-storage.html) as a file hosting.

#### Reason not to build

 [Firefox Send](https://github.com/mozilla/send)  is now much better, and also there is a nice cli [ffsend](https://github.com/timvisee/ffsend)




