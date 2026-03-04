# Markdown ➜ Google Doc (Google Colab)

This Colab notebook converts markdown meeting notes into a well-formatted Google Doc using the Google Docs API.

## Public GitHub Repository
- **Repo link**: `https://github.com/jai-nayani/meeting-notes-to-google-doc`

## Overview
- Creates a new Google Doc programmatically
- Maps headings: H1 (title), H2 (sections), H3 (sub-sections)
- Preserves nested bullets and indentation (ordered + unordered)
- Converts `- [ ]` into real Google Docs checkboxes
- Styles @mentions (bold + color)
- Distinct footer styling (grey)
- Robust retries for transient API errors

## Setup (Colab)
1. Open `Meeting_Notes_to_Google_Doc_Colab.ipynb` in Google Colab.
2. Run the Install cell.
3. Run the Authenticate cell (Colab will prompt you to authorize).
4. Run the conversion cell; a Google Docs link will be printed.
   - Optional: upload your own markdown, or use `examples/product-team-sync.md`.

### Required Scope
- `https://www.googleapis.com/auth/documents`

## Dependencies (installed in the notebook)
- google-api-python-client
- google-auth-httplib2
- google-auth-oauthlib
- markdown-it-py==3.0.0
- beautifulsoup4==4.12.3

## Deliverables
- Working Colab notebook: `Meeting_Notes_to_Google_Doc_Colab.ipynb`
- Example markdown: `examples/original-meeting-notes.md`, `examples/product-team-sync.md`
- README with setup and run instructions

## Evaluation Fit
- Functionality: Creates a fully formatted Google Doc as specified
- Code Quality: Clear structure, meaningful names, humanized comments
- Error Handling: Exponential backoff retries for 429/5xx
- Documentation: This README + inline guidance in the notebook


