# GitStars

Interactive Jupyter notebook for browsing, filtering, curating, and opening your GitHub starred repositories.

## License

This project is licensed under the MIT License. See [LICENSE](C:\Users\chich\Downloads\GitStars\LICENSE).

## Requirements

- Python 3.10+
- A GitHub token in `GITHUB_TOKEN`
- Jupyter Notebook or VS Code with notebook support

## Get a GitHub token

1. Sign in to GitHub.
2. Open [Personal access tokens](https://github.com/settings/tokens).
3. Click `Generate new token`.
4. Choose either `Fine-grained token` or `Tokens (classic)`.
5. For simple use, a classic token is usually easier.
6. Give it a name like `GitStars`.
7. Choose an expiration date.
8. For public starred repos, give it enough access to read your GitHub account data. If you need private repository access, use a token with broader repo read permissions.
9. Copy the token when GitHub shows it.

Important:

- Keep the token private.
- Do not commit the token into this repository.
- If a token is exposed, revoke it in GitHub and create a new one.

## Security

- Never paste your GitHub token into the notebook or any tracked file.
- Prefer setting `GITHUB_TOKEN` only in your current shell session.
- If you accidentally expose a token in code, screenshots, or Git history, revoke it immediately and generate a new one.
- Before pushing this repo to GitHub, review files for secrets.
- If you share downloaded files or saved README files, they should contain repository data only and never your token.

## Setup

Set the token in your shell before opening the notebook.

PowerShell:

```powershell
$env:GITHUB_TOKEN="ghp_your_token_here"
```

Command Prompt:

```cmd
set GITHUB_TOKEN=ghp_your_token_here
```

To check that the token is set:

PowerShell:

```powershell
echo $env:GITHUB_TOKEN
```

Command Prompt:

```cmd
echo %GITHUB_TOKEN%
```

## Open the notebook

Open [GitStars.ipynb](C:\Users\chich\Downloads\GitStars\GitStars.ipynb) in Jupyter or VS Code.

PowerShell:

```powershell
cd C:\Users\chich\Downloads\GitStars
jupyter notebook
```

Then open `GitStars.ipynb`, set your filters in the first cells, and run the notebook from top to bottom.

The notebook lets you:

- list and filter starred repos interactively
- preview a repo README inside the notebook
- open a repo in the browser
- save the README locally
- download the repo as a ZIP
- clone the repo locally

## How to see the code

Open the notebook in VS Code:

```powershell
code C:\Users\chich\Downloads\GitStars\GitStars.ipynb
```

Open the whole project folder:

```powershell
code C:\Users\chich\Downloads\GitStars
```

If you want to inspect the raw notebook JSON in PowerShell:

```powershell
Get-Content C:\Users\chich\Downloads\GitStars\GitStars.ipynb
```

If you want the notebook UI instead of raw JSON, open it in VS Code or Jupyter.

## Suggested workflow

1. Set `GITHUB_TOKEN` in PowerShell or Command Prompt.
2. Open [GitStars.ipynb](C:\Users\chich\Downloads\GitStars\GitStars.ipynb).
3. Run the setup cells.
4. Adjust `QUERY`, `LANGUAGE`, `MIN_STARS`, `SORT_BY`, and `TOP_N`.
5. Pick a repo from the curated results.
6. Preview the README, open it in your browser, download it, or clone it.

## Output files

- `downloads/`: ZIP files downloaded from GitHub
- `clones/`: repositories cloned locally
- `*-README.md`: README files saved from selected repos
