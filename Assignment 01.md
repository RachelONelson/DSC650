---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Rachel Nelson
---

## 1.2 

#### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes       |
| 1024x768 PNG image                         | 1 MB          |
| 1024x768 RAW image                         | 3 MB          | 
| HD (1080p) HEVC Video (15 minutes)         | 879 MB          |
| HD (1080p) Uncompressed Video (15 minutes) | 26400 MB          |
| 4K UHD HEVC Video (15 minutes)             | 45600 MB          |
| 4k UHD Uncompressed Video (15 minutes)     | 30760 MB          |
| Human Genome (Uncompressed)                | 3.436687 GB          |

* 1 byte per character
    * Resource: https://www.unitconverters.net/data-storage/character-to-byte.htm
* Tested by creating images using photopea
    * Resource: https://www.photopea.com/
* Used online video size calculator
    * Resource: https://www.videoproc.com/edit-4k-video/video-size-calculator.htm\
* Human Gnome size found on stack overflow
  * Resource: https://stackoverflow.com/questions/8954571/how-much-storage-would-be-required-to-store-a-human-genome#:~:text=The%20human%20genome%20with%203Gb,or%203.436687%20Gb%20in%20size.



#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64 GB       |   1   |
| Daily Twitter Tweets (Snappy Compressed)  | 43 GB      |    1  |
| Daily Instagram Photos                    | 75 TB      |   23   |
| Daily YouTube Videos                      | 1715 GB       |   1   |
| Yearly Twitter Tweets (Uncompressed)      | 23.4 TB       |   7   |
| Yearly Twitter Tweets (Snappy Compressed) | 15.7 TB    |   5   |
| Yearly Instagram Photos                   | 27.35 PB       |   8213   |
| Yearly YouTube Videos                     | 625.98 TB       |  188    |

* Daily Twitter Tweets (Uncompressed)  
  * 500,000,000 (daily tweets) * 128 (bytes per tweet) =  64,000,000,000 (bytes)/1,000,000,000(bytes to gb)
* Daily Twitter Tweets (Snappy Compressed) 
  * Using 1.5X Compression Rate
  * Resource: https://github.com/google/snappy/blob/master/README.md
* Daily Instagram Photos
  * 100,000,000 (daily posts) * .75 (% of images) = 75,000,000 MB (1 MB per photo) or 75 TB
  * 75 TB (photos) * 3 (copies of each piece of data) = 225 TB/10 TB Per Hard Drive = 23
* Daily YouTube Videos
  * 500 (Hours of Video) * (3.43 GB per hour file size) = 1715 GB 
  * 1715 GB * 3 (copies of each piece of data) 5145 GB = / 10000 (GB in a HD)
* Yearly Twitter Tweets (Uncompressed)  
  * 64 GB (daily twitter) * 365 (days in a year) = 23.36 TB
  * 23.36 * 3 (copies of each piece of data) = 70 TB / 10 1B per hard drive
* Yearly Twitter Tweets (Snappy Compressed) 
  * 43 GB Daily * 365 = 15.695 TB
  * 15.695 TB * 3 (copies of each piece of data) = 47.085 TB / 10 TB per HD
* Yearly Instagram Photos
    * 75 TB Daily * 365 = 27.345 PB or 27375 TB
    * 27375 TB * 3 (copies of each piece of data) = 82125 / 10 TB per HD = 2812.5
* Yearly YouTube Videos
  * 1715 GB * 365 = 625.975 TB
  * 625.975 * 3 (copies of each piece of data) = 1877.925/10 TB per HD = 187.7925


#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | 7   |    <1        |
| Twitter Tweets (Snappy Compressed) | 5   |      <1      |
| Instagram Photos                   | 8213   |     73       |
| YouTube Videos                     | 188   |       2     |

* Estimated based on Failure rate of 0.89% (# HD * 0.89%)

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 30 ms                 |
| Low Earth Orbit Satellite | 1-6.67 ms                 |
| Geostationary Satellite   | 120 ms                 |
| Earth to the Moon         | 1281.571 ms                 |
| Earth to Mars             | 3.03 minutes            | 

* Los Angeles to Amsterdam 
  * 5,551 miles * 1.60934 km/mile = 8993.446 km * 1000 / 300000 (speed of light) = 29.978
  * Resource: https://www.google.com/search?q=distance+between+la+and+amsterdam&rlz=1C1CHBF_enUS913US913&oq=distance+between+la+and+amberstam&aqs=chrome.1.69i57j33i10i160.12942j0j4&sourceid=chrome&ie=UTF-8
* Low Earth Orbit Satellite
  * 250 km (lowest LEO Satellite) * 1000 / 300000 (speed of light) = .8333
  * 2000 km (highest LEO Satellite) * 1000 / 300000 (speed of light) = 6.67
  * Resource: https://www.google.com/search?q=Low+Earth+Orbit+Satellite+distance&rlz=1C1CHBF_enUS913US913&ei=7b2rYYKiHs-s0PEPlv66uAY&ved=0ahUKEwjCzMSW7cr0AhVPFjQIHRa_DmcQ4dUDCA4&uact=5&oq=Low+Earth+Orbit+Satellite+distance&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEIAEMgYIABAWEB4yBQgAEIYDMgUIABCGAzIFCAAQhgMyBQgAEIYDMgUIABCGAzoHCAAQRxCwAzoHCAAQsAMQQzoECAAQQzoICAAQgAQQyQM6BQguEIAESgUIPBIBMUoECEEYAFD0BFiUDGDdD2gBcAJ4AIABV4gBzQWSAQE5mAEAoAEByAEKwAEB&sclient=gws-wi
* Geostationary Satellite
  * 36,000 km (lowest LEO Satellite) * 1000 / 300000 (speed of light) .8333
  * Resource: https://www.google.com/search?q=Geostationary+Satellite+distance&rlz=1C1CHBF_enUS913US913&ei=8b2rYf_uDqL59AOw6pnoDg&ved=0ahUKEwi_q6mY7cr0AhWiPH0KHTB1Bu0Q4dUDCA4&uact=5&oq=Geostationary+Satellite+distance&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEIAEMgUIABCABDIGCAAQFhAeMgUIABCGAzIFCAAQhgMyBQgAEIYDOgcIABCxAxBDOgQIABBDOgUIIRCgAUoFCDwSATRKBAhBGABQAFiOHGCGHWgEcAJ4AYAB4wGIAcULkgEGMTEuMS4ymAEAoAECoAEBwAEB&sclient=gws-wiz
* Earth to the Moon
  * 238,900 Miles * 1.60934 km/mile = 384471.3 * 1000 / 300000 (speed of light) = 1281.571
  * Resource: https://www.google.com/search?q=earth+to+the+moon+distance&rlz=1C1CHBF_enUS913US913&ei=gMCrYYG1E6Ha9AOGjJygAQ&oq=earth+to+the+moon+dis&gs_lcp=Cgdnd3Mtd2l6EAMYADIJCAAQQxBGEPsBMgUIABCABDIFCAAQgAQyBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjoHCAAQRxCwAzoHCAAQsAMQQzoKCC4QyAMQsAMQQzoFCC4QgARKBQg8EgExSgQIQRgAULUFWP0HYIwSaAFwAngAgAFTiAGzApIBATSYAQCgAQHIAQ_AAQE&sclient=gws-wiz
* Earth to Mars
  * 54.6 KM * 1000 / 300000 (speed of light) = 182000 = 3.03333333 minutes
  * Resource: https://www.google.com/search?q=earth+to+mars+in+km&rlz=1C1CHBF_enUS913US913&ei=lr-rYf7CCozF0PEP6ImG0AU&ved=0ahUKEwj-5YTh7sr0AhWMIjQIHeiEAVoQ4dUDCA4&uact=5&oq=earth+to+mars+in+km&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEIAEMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgUIABCGAzIFCAAQhgMyBQgAEIYDOgcIABBHELADOgcIABCwAxBDOgkIABBDEEYQ-wE6BAgAEENKBQg8EgExSgQIQRgAUKUHWPQNYJwPaAFwAngAgAFViAHYA5IBATaYAQCgAQHIAQrAAQE&sclient=gws-wiz
  
