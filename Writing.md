I very much recommend that you read through the material available at [Celia Elliot's webpage](https://physics.illinois.edu/people/directory/profile/cmelliot). 
Her talks have a lot of detail on each of these topics.

## Collaboration
 * Set up a private GitHub repository
 * Commit all plotting and analysis scripts to the repository 
 * If data is less than a few MB, also put it in the repository. If it's big, provide a link to it.
 * Do not commit .aux and the paper PDF. Figure PDFs are ok.
 * Commit immediately after making a change

I often randomly get time to look at papers. 
For example, right before getting on a plane, I'll loop through the paper repositories and `git pull` them all.
If your paper hasn't changed, I won't look at it and the paper will be delayed more than it needs to be.

## File structure
```
+-- 0_outline
|   +--  outline-[papername].tex
|   +--  [papername].bib
+-- 1_draft
|   +-- [papername].tex
|   +-- [papername].bib
+-- 2_plots
|   +-- fig_[useful name].pdf
|   +-- plot_[useful name].py
+-- 3_data
|   +-- [tablename].csv
|   +-- [tablename].hdf5
+-- 4_submit
|   +-- [papername].tex
|   +-- [papername].bib
|   +-- [papername].pdf
|   +-- fig_[useful name].pdf
|   +-- ...
+-- 5_response
|   +-- response-[papername].tex
+-- 6_resubmit
|   +-- [papername].tex
|   +-- [papername].bib
|   +-- [papername].pdf
|   +-- fig_[useful name].pdf
```

  * papername should have something to do with the paper. That way when we make PDFs they aren't all manuscript.pdf.:)
  * We commit the submitted PDFs so that they are recorded, but not the draft versions. **Do not** commit paper PDFs until you hit the submit button on the publisher's website.
  * The plotting files should have the same name as the figures they produce. 
  
## The TeX file
 * One line per sentence
 * Use colored comments, e.g.: 
 ```latex 
 \newcommand{\lucas}[1]{\textcolor{blue}{\bf [LKW: #1 ]}} 
 ```
One line per sentence helps git properly track changes. The colored comments let us easily mark things to consider later without forgetting about them. 
 
## Writing order
 * "True statements"
 * Outline
 * Figures
 * Text

**True statements** are clear, concise statements of fact. 
We build our paper around these true statements. 
An example: 
  * "If the effective energy functional equals the ab-initio energy functional in the low-energy space, then the effective Hamiltonian will share energy eigenstates with the ab-initio one."

It's ok to write down statements you think might be true, although you should probably mark them as being uncertain.
These statements can be things that seem trivial to you at the time, but they will be building blocks for our argument.
There will likely be a lot of revision on these statements.

The **outline and figures** are often developed at the same time. 
Figures will typically be related to the true statements developed above. 
Every statement of fact should be backed up by a citation, figure, table, or a proof. 
The outline will eventually become the topic sentences of each paragraph.

When writing the **text**, use the outline sentences as topic sentences of each paragraph. 
The paragraph's entire purpose is to support the statement of fact, and to lead to the next topic sentence.
Any digressions from this purpose should be omitted. 

## Introductions 
Paper and talk introductions roughly consist of four parts. In a paper, these parts will usually be one paragraph each. 
 * Overall goal 
 * Barrier to achieving that goal
 * Current state of the art to overcoming that barrier
 * Our advancement of that state of the art
 
## Writing tips
 * Your outline gives you the topic sentences for each paragraph
 * The purpose of a paragraph is to draw a direct line from its topic sentence to the topic of the next paragraph
 * Avoid extraneous details and parenthetical comments. 
 * If you're not a native speaker, use a grammar checker (https://www.grammarly.com) or ask a native speaker to check your English before sending it to me.
 * Avoid filler words such as "various," "strong," "weak," "small," "good agreement," and so on.
 * Avoid sentences that start with words such as "moreover" and "also"; that usually means that you have not thought through what you want to say.

## Making figures 
 * In matplotlib, set figsize=(3,3) for one column, otherwise the size you want it.
 * Set the font size around 10-11
 * Do not use the width parameter in \includegraphics
 * Don't worry about figure placement while you're writing the document; usually it automatically adjusts once there's enough text.

## Writing responses
 * Make a tex file with the referee comments copied.
 * Surround each referee comment with the following command:
 ```
 \newcommand{\referee}[1]{\textcolor{blue}{\textit{#1 \\}}}
 ```
  * Write your response to each referee comment below theirs. Suggest changes to the manuscript here. Do not make any changes to the manuscript yet.
  * Discuss the changes with your coauthors and agree whether those changes are warranted and address the referee comments.
