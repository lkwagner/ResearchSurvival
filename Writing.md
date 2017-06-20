
## Collaboration
 * Set up a private GitHub repository
 * Commit all plotting and analysis scripts to the repository 
 * If data is less than a few MB, also put it in the repository. If it's big, provide a link to it.
 * Do not commit .aux and the paper PDF. Figure PDFs are ok.
 * Commit immediately after making a change
 
## The TeX file
 * One line per sentence
 * Use colored comments, e.g.: \newcommand{\lucas}[1]{\textcolor{blue}{\bf [LKW: #1 ]}} 
 
## Writing order
 * Outline
 * Figures
 * Text

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
 * Avoid poorly defined or vague words like "various," "strong," "weak," "small," "good agreement," and so on.
 * Words like "moreover" usually mean that you are off the plot

## Making figures with minimal sweat
 * In matplotlib, set figsize=(3,3) for one column, otherwise the size you want it.
 * Set the font size around 10-11
 * Do not use the width parameter in \includegraphics
 * Don't worry about figure placement while you're writing the document; usually it automatically adjusts once there's enough text.
