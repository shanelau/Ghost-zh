# Privacy

This is a plain English summary of all of the components within Ghost which may affect your privacy in some way. Please keep in mind that if you use third party Themes or Apps with Ghost, there may be additional things not listed here.

Each of the items listed in this document can be disabled via the `config.js` file. Please see the the [configuration guide](http://support.ghost.org/config/) in the support documentation for details.

## Official Services

Some official services for Ghost are enabled by default. These services connect to Ghost.org and are managed by the Ghost Foundation: the Non-Profit organisation which runs the Ghost project.


### Automatic Update Checks

When a new session is started, Ghost pings a Ghost.org endpoint to check if the current version of Ghost is the latest version of Ghost. If an update is available, a notification appears inside Ghost to let you know. Ghost.org collects basic anonymised usage statistics from update check requests.

This service can be disabled at any time. All of the information and code related to this service is available in the [update-check.js](https://github.com/TryGhost/Ghost/blob/master/core/server/update-check.js) file.


## Third Party Services

Ghost uses a number of third party services for specific functionality within Ghost.


### Google Fonts

Ghost makes use of the Open Sans [Google Font](https://www.google.com/fonts), which is loaded into the Ghost admin area to provide a typographically stimulating experience.

### Gravatar

To automatically populate your profile picture, Ghost pings [Gravatar](http://gravatar.com) to see if your email address is associated with a profile there. If it is, we pull in your profile picture. If not: nothing happens.

### RPC Pings

When you publish a new post, Ghost sends out an RPC ping to let third party services know that new content is available on your blog. This enables search engines and other services to discover and index content on your blog more quickly. At present Ghost sends an RPC ping to the following services when you publish a new post:

- http://blogsearch.google.com
- http://rpc.pingomatic.com

RPC pings only happen when Ghost is running in the `production` environment.

### Sharing Buttons

The default theme which comes with Ghost contains three sharing buttons to [Twitter](http://twitter.com), [Facebook](http://facebook.com), and [Google Plus](http://plus.google.com). No resources are loaded from any services, however the buttons do allow visitors to your blog to share your content publicly on these respective networks.


### Structured Data

Ghost outputs Meta data for your blog that allows published content to be more easily machine-readable. This allows content to be easily discoverable in search engines as well as popular social networks where blog posts are typically shared.

This includes output for post.hbs in {{ghost_head}} based on the Open Graph protocol specification.