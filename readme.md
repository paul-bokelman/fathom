Fathom: A tool to help you get a better understanding of any subject you want to learn.

### Core Features

- **Inquisitive**: Similar to talking to a curious student or peer, Fathom will continually ask questions about its lack of understanding of the subject, forcing you to thoroughly and completely explain the concept.
- **Compilation**: Talk freely, and let Fathom compile the information into an optionally user-defined structured format for later reference.

### Philosophy

There's a difference between knowing and understanding a concept or idea. Explaining a concept verbally allows you to elevate your unconscious understanding to your conscious state. This elevation allows for critical thinking of the unconscious information in the domain of the consciousness. Additionally, by explaining a concept to peers you are forced to identify the errors and inconsistencies in your own understanding leading to a rich iterative process that hones in a more holistic view of the concept/subject.

### Usage

1. Clone repo
2. Add your Anthropic API key to the .env file with the key `ANTHROPIC_API_KEY`
3. OPTIONAL: Create virtual environment with `python -m venv venv` and install packages (requirements.txt)
   - Activate environment: `source venv/bin/activate` or `venv/Scripts/activate` (Windows)
   - Install packages: `pip install -r requirements.txt`
4. OPTIONAL: Tweak 'constants' as needed, notably:
   - Add compilation templates under /templates
   - Control max audio length
   - Adjust max number of output tokens for each mode
   - Preferred input type
5. Run with `python main.py` in selected environment or `venv/bin/python main.py`

### Additional Information

#### Compilation Templates

Custom templates use special blocks to inform the AI where to put certain information. A breakdown of the included `basic-notes.md` is as follows:

```md
# {{Header}} // Signifies the main purpose of the topic (appears once)

## {{Subsection}}... // Any subsection of the topic (appears multiples times because of '...')

- {{Point}}... // Any piece of information related to the subsection (appears multiples times because of '...')

## Questions

+Generate some thought provoking questions based on the notes+ // custom prompt that is answered and replaced by the AI
```
