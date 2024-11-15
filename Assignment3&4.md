# Assignment 3 & 4: Critique by Design with Tableau (MakeoverMonday)
## Feedback  
In this section, I documented feedback my interviewer gave me.  
- **Person 1** (My Friend 23. Technical Background)  
- **Person 2** (My Relative 50. Non-Technical Backgroud)
  
These are the question I asked and their response.  
  
**Can you tell me what you think this is?**  
  - **Person 1** : *This is LLMs based on their MMLU scores and announcement dates, but what is the size about? He is also happy to know NIVIDIA now has LLM.*  
  - **Person 2** : *She thinks this is a fancy graph said I did a good job, then she questioned what is large language model and what is MMLU.*
    
  - **Takeaway:** At first I didn't place a subtitle about what is the size about, after this I made a specific context about size.
          Also, when trying to explain something to non-technical background audience, jargon should be avoided, this is very important.
          But I think person 2 is not my target audience, so I didn't add too much explaination on the terminology, which will take up too much space.
    
**Can you describe to me what this is telling you?**  
  - **Person 1**: *He understood that the chart shows the progression of LLMs over time in terms of size and performance, but he suggested adding more details on how MMLU scores relate to real-world applications. Which is one point I missed from the original chart. In the original chart, it says when MMLU reaches 88.9, it represents human expert.*  
  - **Person 2**: *She said it seems like companies are building more powerful models, but she was confused about what exactly "performance" means here and how to read the chart.*

  - **Takeaway:** While technical viewers may grasp the overall trends, they may still appreciate additional context on how metrics like MMLU are practically relevant. Non-technical viewers, however, may find terms like "performance" confusing and need simplified explanations. Both technical and non technical audience is kind of confused about what is this metric means. How "performance" is related to some real-life scenario, I added a tag on y-axis. Saying above 70 is ideal, and 88.9 is expert.

**Is there anything you find surprising or confusing?**  
  - **Person 1**: *He liked the black boundary around overlapping areas, as it helps distinguish models that overlap.*  
  - **Person 2**: *She focused on the bright colors and big company names, saying they look impressive and even mentioned it'd be amazing if I could work at one of these companies.*  

  - **Takeaway:** The black boundary around overlapping areas is effective for improving clarity, especially for technical viewers, they may be detailed-oriented. For non-technical viewers, visual appeal and recognizable company names draw attention, but their focus is less on data specifics. This shows that aesthetic elements can enhance engagement even for those less familiar with the subject. They also mentioned MMLU, this is the most confusing part.
 
**Who do you think is the intended audience for this?**  
  - **Person 1**: *LLM engineer, Data Scientist, he says this is useful becuase he can clear tell which model achieve best performance with least parameters*  
  - **Person 2**: *Analyst, she says understanding the trends are useful. People can pick the best model.*  

  - **Takeaway:** Both technical and non-technical viewers recognized that the intended audience is data scientists or technical professionals.

**Is there anything you would change or do differently?**  
  - **Person 1**: *He suggested creating a more detailed, zoomed-in version.*  
  - **Person 2**: *She said she trusts my judgment and left it up to me.*
  - **Takeaway:** Technical viewers may appreciate a more detailed or interactive version. Non-technical viewers, on the other hand, are generally satisfied with the current presentation and rely on overall readability.


### Key Takeaways from Feedback
- **How to Avoid Overlap**: In order to avoid overlap, I applied few filters and ensure my audience and zoom in, play with this visualization, if they want a overview, they can drag the filter to a border range, if they want a more specific, detailed version, they can zoom in.
- **Clear context**: I added serveral subtitles and tag on the y axis in order to provide more context to my data visualization.
- **Less Information is better**: Through the conversation, I realized what professor said, sometimes fewer information is better, considering this graph, which is about LLM, there are so many LLMs and when putting these tag together, it produces a mess, therefore, I only chose 5 companys to make my visualization looks more "CLEAN". Also, I changed x-axis to quater while original visualization uses year, using quater as my x-axis produces more space between these circles.

[Back to README.md](README.md)
