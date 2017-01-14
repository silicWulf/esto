# esto - An e621 API wrapper

esto is an easy-to-use e621 API wrapper, with a goal of covering the entirety of the e621 API in a simple form.

## Functions (0.0.1)

As of 0.0.1, the module has two simple functions: getting a file object, and downloading a file object automatically, both accepting tags as parameters.

In addition, the module currently uses the `requests` module to post requests to the API. In the future the `requests` module will not be required.

### esto.e621File
An `e621File` object.
 * `id` -- post id (str) 
 * `tags` -- tags associated with the post (str)
 * `description` -- post description (str)
 * `creator_id` -- poster id (str)
 * `author` -- name of post author (str)
 * `change` -- change id (int)
 * `score` -- post score (int)
 * `fav_count` -- favorites count (int)
 * `md5` -- md5 hash of file (str)
 * `file_size` -- file size in bytes of the file (str)
 * `file_url` -- file url (str)
 * `file_ext` -- file extension, ex. jpg, png, etc. (str)
 * `preview_url` -- image preview url (str)
 * `preview_width` -- width of the image preview (int)
 * `preview_height` -- height of the image preview (int)
 * `sample_url` -- sample preview url (str)
 * `sample_width` -- width of the sample preview (int)
 * `sample_height` -- height of the sample preview (int)
 * `rating` -- rating of file (e = explicit, q = questionable, s = safe) (str)
 * `status` -- status of the post, ex. pending, accepted, etc. (str)
 * `width` -- width of the image (int)
 * `height` -- height of the image (int)
 * `has_comments` -- whether or not the post has comments [as of 0.0.1, comments are not given with the wrapper] (boolean)
 * `has_children` -- whether or not the post has children [as of 0.0.1, children are not given with the wrapper] (boolean)
 * `children` -- post ids that are children of the requested post, returns empty string if none (???)
 * `parent_id` -- id of the parent post, returns None if none (???)
 * `artists` -- list of artists of the file (list) 
 * `sources` -- list of sources of the file (list)

### esto.getdata(tags)
Returns an `e621File` object with data retrieved from the API.
 * `tags` -- can either be a list of tags or a single string, with tags seperated by spaces.

### esto.downloadfile(tags, filename)
Downloads a file with the tags `tags` locally at `filename`.
 * `tags` -- can either be a list of tags or a single string, with tags seperated by spaces. (list/str)
 * `filename` -- local path for file (str)
