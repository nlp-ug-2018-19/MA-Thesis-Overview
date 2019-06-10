### Analyzing the structure and effectiveness of news headlines using NLP
-   Posted by [Mike Waldron](https://www.datasciencecentral.com/profile/MikeWaldron) on June 9, 2016 at 1:30am

_We wanted to gather and analyze news content in order to look for similarities and differences in the way two journalists write headlines for their respective news articles and blog posts. The two reporters we selected operate in, and write about, two very different industries/topics and have two very different writing styles:_

-   **Finance:** Akin Oyedele of Business Insider, who covers market updates.
-   **Celebrity:** Carly Ledbetter of the Huffington Post, who mainly writes about celebrities.
 ![Akin Oyedele and Carly Ledbetter
]([https://66.media.tumblr.com/978efd3b038dee7d0364105ffde292ea/tumblr_inline_o6elyj52xr1u37g00_500.png])

### The Approach

*  Collect news headlines from both of our journalists
*  Create parse trees from collected headlines (we explain parse trees below!)
*  Extract information from each parse tree that is indicative of the overall headline structure
*  Define a simple sequence similarity metric to quantitatively compare any pair of headlines
*  Apply the same metric to all headlines collected for each author to find similarity
*  Use K-Means and tSNE to produce a visual map of all the headlines so we can clearly see the differences between our two journalists
### Data

In total we gathered about 700 article headlines for both journalists using the [AYLIEN News API](https://t.umblr.com/redirect?z=https%3A%2F%2Fnewsapi.aylien.com%2Fdemo&t=YzYzNmZiYzZjOTlmNTZlZjc1MWM1ZDNhMWRlYmVjMDIzYzdiY2NjMSxKdXNPMVRLVg%3D%3D) which we then analyzed using Python. If you’d like to give it a go yourself, you can grab the Pickled data files directly from the GitHub repository (link), or by using the data collection notebook we prepared for this project.

>First we loaded all the headlines for Akin Oyedele, then we created parse trees for all **700** of them, and finally we stored them together with some basic information about the headline in the same Python object.

Then using a sequence similarity metric, we compared all of these headlines two by two, to build a _similarity matrix_.
