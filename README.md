## Why?
just a test to see how many of these images looks good out of a 1000 i scraped, i also needed some images to apply some filters to so this website seemed a great choice since none of these pictures are from real people

## How?
just did a quick search and found a one liner to download these, ran it thru a for loop, keeping in mind to not hammer the server very hard and applying some sleep time between each image download
```
for i in {0001..1000} ; do curl 'https://thispersondoesnotexist.com/image' -H 'authority: thispersondoesnotexist.com' -H 'cache-control: max-age=0' -H 'dnt: 1' -H 'upgrade-insecure-requests: 1' -H 'user-agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36' -H 'sec-fetch-mode: navigate' -H 'sec-fetch-user: ?1' -H 'accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3' -H 'sec-fetch-site: none' -H 'referer: https://thispersondoesnotexist.com/' -H 'accept-encoding: gzip, deflate, br' -H 'accept-language: en-US,en;q=0.9' --output $i.jpg ; sleep 3 ; done
```
please if you want to do this yourself be sure to apply the sleep time of at least 1 seconds between each image grab to not overwhelm the servers

## Things i removed
glitched images, uncanny images and images of children are removed, out of 1000 images there is 581 images left which is about 58% good images which i find a very good result

## How to download?
either use the auto generated [zip file](https://github.com/junguler/TPDNE_example_images/archive/refs/heads/main.zip) or run a git clone
```
git clone https://github.com/junguler/TPDNE_example_images.git
```
