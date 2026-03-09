# Eleventy Base Blog for 11tyCMS
This is a fork of 11ty's [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) designed for 11tyCMS. By default, 11tyCMS _is_ compatible with `eleventy-base-blog`, but there's a missing folder for media and unsupported nested collections. This fork aims to give an example of what 11tyCMS will work with.

## How do I configure this for 11tyCMS?
Simply open the directory in 11tyCMS, and the welcome wizard will open. Set it up with the following settings:
<img width="500" alt="Screenshot of the settings required. Input/content is set to 'content', Includes folder is set to '_includes', Media uploads is set to 'content/media', Data folder is set to '_data' and Output folder is set to '_site'" src="https://github.com/user-attachments/assets/adc7f0bd-6014-4e1f-8dc6-9c4bbe79eeb5" />

Finally, for the publish command, set it to whatever command you'd use to publish your site. A few I use:
**For Git:**
`git add . && git commit -a -m \"$(git status --short | sed 's/^...//g' | paste -sd ', ' -)\" && git push`
**For Neocities:**
`neocities push .`

Bare in mind, the publish command runs in your output folder.

If you don't have a publish command in mind, just set it to: "echo hello".

## How does media work?
Whenever you use the "image upload" function in 11tyCMS, it will put that image inside the media folder you specified. In this templates case, that is: "content/media"
