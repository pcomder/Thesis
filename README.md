import json, os

nb_path = "/mnt/data/Untitled7.ipynb"
with open(nb_path, 'r', encoding='utf-8') as f:
    nb_json = json.load(f)

code_cells = [cell for cell in nb_json['cells'] if cell.get('cell_type') == 'code']
full_code = "\n\n".join("".join(cell.get('source', '')) for cell in code_cells)

out_path = "/mnt/data/esg_panel_analysis.py"
with open(out_path, "w", encoding="utf-8") as f:
    f.write(full_code)

print(f"Code extracted to: {out_path}")
