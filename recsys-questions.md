# Questions to ask about your Recommender Systems
So, you're building a Recommender System that connects your users with the right content on your platform. Consider asking these practical questions that can help avoid costly mistakes and help you build user trust with your RecSys.

## Content Related Questions
Content understanding in the context of Recommender Systems refers to the process of extracting and interpreting meaningful data from the content itself, which is then used to inform the recommendations. This is an essential part of building effective recommendation algorithms that can provide relevant, personalized content for users. Here are a few practical questions to ask about your content:

**Question 1: What features and characteristics can we use to best describe and group content?** Can these groupings form a natural hierarchy? For example, movies can be grouped by genres (_Drama_) and subgenres (_Medical Drama, Political Drama_). Content topology of this nature is important when the system needs to present content that is either similar, or distinct from what the user has already been exposed to.  


**Question 2: What is the smallest unit of content, and is it uniquely identifiable within the system**. While this is an obvious question, it is important that we understand and uniquely identify the different variations of a piece of content. For example, in an e-commerce platform, the smallest unit of content is the SKU, which represents the product (_LuxeBrand Sectional_) + it's features (_Beige, L-Shaped Right_).


**Question 3: How is content quality defined and assessed?** The adage "garbage in, garbage out" is especially true in Recommender Systems. Quickly identifying low-quality content and down-ranking or outright filtering them out of the system goes a long way in building and maintaining user trust in recommended content.


**Question 4: Is there content that should not be recommended for legal or ethical reasons?** Similar to the previous question, it is important to define within the system what types of content are illegal or unethical to recommend. A human-in-the-loop team dedicated to **Trust and Safety** is an important component of a Recommender System. Set this team up early and empower them, otherwise be ready for potential user attrition and/or legal challenges that may follow.


**Question 5: What contexts, surfaces or channels should we avoid applying personalization techniques?** For example, while I appreciate and probably expect personalization in Spotify-owned playlists, I certainly do not want Spotify re-ranking my private, carefully curated playlists, and if they do, it should be an opt-in experience.


**Question 6: Is there a seasonality dimension to your content?** If so, ensure to capture seasonality attributes on your content. For example, Christmas related content should be tagged as such within the system. There's only a shortlist of things more annoying than receiving personalized emails from your favorite shopping site for Christmas deals in February of the following year.


**Question 7: Will users be ok with consuming the same piece of content multiple times?** Most users on Apple Music probably listen to the same 10 tracks on repeat day after day. On the other hand, if I purchased a couch on Overstock.com, showing me recommendations for the same couch, or any couch for that matter is probably a waste of RecSys resources. It is important to understand this user-content relationship within your Recommender System.


**Question 8: What signals should we use to mark a piece of content as no longer to be recommended?** For example, in an e-commerce platform, a _purchase_ is a signal that a user will likely no longer engage with that content as well as content in the same class grouping. In some systems, it may be appropriate to down-rank the content, while in others, filtering out the content is the right approach. It is also important to define how long after penalizing a piece of content should it be ok to re-introduce to a user.

## User Related Questions
User understanding in the context of Recommender Systems refers to the system's ability to accurately interpret and predict user preferences, behaviors, and intent based on various types of data collected about the user. This concept is central to improving the relevance and personalization of recommendations. Consider asking the following questions:

**Question 9: What kinds of information SHOULD NOT be collected about users, for legal or ethical reasons?** To better understand users, we have to capture _a lot_ of information about their habits on the platform. But more important than what information we collect, is what we SHOULD NOT collect. You'd want to get Legal, as well as Trust and Safety heavily involved early on when it comes to what types of user information to collect, how it is stored, who has access to this information, and how much control users have over the data you collect about them. GDPR compliance is no joke!

**Question 10: Can a user consume your content without being logged in?** Let's say users can consume your content without being logged in, so called _anonymous users_. Now you have to worry about user identity reconciliation. Can you perform device matching to tie the user session to a known user? _Should you?_ Can you use the user's geoip to offer relevant content? _Should you?_ There's different techniques to explore in this scenario, the point here is to be thinking about this use case if it applies to you.

**Question 11: Are you explaining to users why you recommended a given piece of content?** Explaining to users why they're getting a particular recommendation (_Recsplaining_) is important for building trust and can even help drive engagement with the RecSys. Recsplanations such as _Because you follow..._, _Because you liked..._ are indicators that help frame a user's expectations when engaging with recommended content. UX writers are a must-have.

**Question 12: Is content localization a major factor to be considered?** A user who understands only English language will likely not get any value from a recommended Coursera course where the instructor communicates in Mandarin, even if the content of the course closely matches their taste.

**Question 13: Does your UI allow for creating different surfaces for different user intent?** Understanding _user intent_ is the holy grail of Recommender Systems. User intent could change from day-to-day, session-to-session or even second-to-second. It's hard to tell if the user is in a discovery mode (_they want new things_) or if they want the same old content they've been consuming. One way to address this via UI/UX, is by providing prominent surfaces tailored to different user intent. Common examples are:
 * A _search bar_ at the top of the home page, so users can quickly search exactly what they want.
 * A _Recently Viewed_ section, so users can quickly jump back into familiar content.
 * An _explore tab_, so users can be exposed to new or related content. etc.

## Business Related Questions
Recommender Systems aim to balance multiple objectives - user, content creator, and business objectives. Afterall, if the system can't help the business achieve its objectives, it's quite simply a waste of resources. Here are a few business related questions to ask:

**Question 14: Are you building multiple isolated Recommender Systems?** As your business grows, inevitably, you will want to enact certain business decisions that affect all recommendations in your product. Maybe you want to increase consumption of NFT-related products because they have higher margins. If you have multiple isolated recommender systems, sweeping business decisions become slow to implement. Consider leveraging shared libraries, or a more centralized RecSys platform, so wide-reaching business decisions can be implemented in week(s), not months. 