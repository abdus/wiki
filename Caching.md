Caching is the process of storing data temporarily. a cache generally lives for
a relatively small amount of time. examples: browser cache, DNS caching etc.

## Reason to Utilize Caching

- **save bandwidth (and reuse resources)**: when using cache mechanism in 
  client-side applications, it ensures that cached files won't be downloaded
  again from the server.
- **save processing power**: when writing algorithms, it could be optimized 
  using a caching mechanism caching would help add memorization to that 
  algorithm, enabling it NOT to repeat the same calculations again and again.
- **save time**: we all visit websites mostly by domain names(and rarely using
  the IP address). having cached DNS records would let the resolver use he
  previous lookup results and save us some time.

So, caching has so many advantages. should we use it for everything? Nope! 
that's a bad idea.

### Trade-Offs

- **disk space**: storing data needs some sort of space on the user's device.
  caching won't make sense if we dump everything in the user's device.
- **stale resources (old resources)**: whatever data has been cached, may not
  be the latest copy.
- **complexity**: depending on where you are using a cache mechanism, it may
  not be straightforward.

### Type of Resources to be Cached(in context to Web Development)

it highly depends on the developer to decide what to cache and what not to.
for instance, static files which does not change frequently, are good to be
cached.

another example: in a chat app, old chats can be cached. basically, anything
that reduces server-load without affecting user experience badly, can be
cached :)
