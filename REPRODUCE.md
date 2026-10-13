# Reproduce the Sankey generator

The original Python generator was buried inside the repository ZIP. It is now available as `create_sankey.py`, with an explicit CLI, input validation, and a synthetic example. The original saved HTML files and ZIP remain unchanged.

```bash
python -m pip install -r requirements.txt
python create_sankey.py examples/synthetic_workshops.csv output/demo.html
```

Open `output/demo.html` in a browser. Plotly, fonts, and CSS load from external CDNs, so rendering requires network access. The four example rows are deliberately synthetic; they are not workshop applicants or evidence of workshop outcomes.

For real data, provide an authorized CSV containing `Workshop` and categorical attributes. The HTML embeds the selected record-level data, so review what will be included before publishing a generated file. The original ZIP contains raw and processed workshop datasets; public-sharing authorization and the existing README's GDPR assertion have not been verified in this repair pass.

Generation and input validation are tested locally. Interactive browser behavior and the existing workshop visualizations still need visual verification.
