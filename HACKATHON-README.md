# Project name

Commonality

## Team Members

Fraser Crichton: [linktr.ee/frasercrichton](https://linktr.ee/frasercrichton)

## Tool Description

A far from elaborate Jupyter Notebook that interrogates the output of Jordan Wildon's Telepathy command line tool for common hyperlinks between Telegram Channels. 

Modelling the connections between different groups using Telegram is I think useful for some of the research I'm doing at the moment as although a group may work to distance itself from a more extreme group it's important to be able to find data that shows their shared interests and perspectives on the world. Hyperlinks - or the content they link to - is just one way of doing this.

## Installation

Follow the instructions in the Project [README.md](README.md). 

## Usage

The tool will identify hyperlinks that are present between two Telegram channels. 

Run a `--comprehensive` search in the Telepathy command line tool. For Example:

`python3 telepathy/telepathy.py --target durov --comprehensive`

Run another comprehensive. For Example:

`python3 telepathy/telepathy.py --target telegramtips --comprehensive`

You should now have a directory: [./telepathy/](./telepathy/) which will contain sub directories named after the channels you have searched for.

Launch the [Commonality.ipynb](./analysis/Commonality.ipynb) Jupyter Notebook (For running note books see here for more info: [https://docs.jupyter.org/en/latest/running.html](https://docs.jupyter.org/en/latest/running.html))

You'll change the cell in the notebook that looks like this:

```
telegram_file_1 = '../telepathy_files/' # update this with your file!
telegram_file_2 = '../telepathy_files/' # update this with your file!

# Example
# telegram_file_1 = '../telepathy_files/durov/durov_2022_09_25-10_14_archive.csv'
# telegram_file_2 = '../telepathy_files/telegramtips/telegramtips_2022_09_25-10_39_archive.csv'
```

- `telegram_file_1` add the location of the first csv file
- `telegram_file_2` add the location of the second csv file


Run the cell.

Run the next cell to get the results. 

## Additional Information

Yeah, sorry this is pretty terrible. Had I more time I'd work on:

- identifying shared members between groups 
- shared people forwarding messages into groups (edgelists)
- topic mapping the messages to identify shared themes
- I'd remove the CLI and run it all from Jupyter Notebooks instead of the mix of command line and notebook 
- more analysis 
- visualisation
 
I've already done some work there that I can share privately if you are interested but have a long way to go.

I'd hoped to find a team to contribute to but that hasn't worked out.   
