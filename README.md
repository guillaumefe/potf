# Project On The Fly (POTF)

**POTF** is a lightweight, client-side project planning tool that helps you define requirements, add actions with RACI roles, and export an Excel file with project data, Gantt chart, and RACI matrix.

## Features

- Assign actions to requirements
- Assign RACI roles (Responsible, Accountable, Consulted, Informed)  
- Quick KPI dashboard (project stats and error tracking) 
- Excel export: `Data`, `Gantt`, `RACI`  
- No backend  
- Auto-save state in the browser (IndexedDB)  

## Usage

1. Set project start date  
2. Enter one requirement per line  
3. Add actions per requirement  
4. Assign R/A/C/I roles  
5. Export to Excel via **Generate Gantt**

## Run locally

```bash
git clone https://github.com/your-username/project-on-the-fly.git
cd project-on-the-fly
python3 -m http.server
```

Then open `http://localhost:8000` in your browser.

## Stack

- **Libraries**:  
  - [`ExcelJS`](https://github.com/exceljs/exceljs) – for creating `.xlsx` files  
  - [`FileSaver.js`](https://github.com/eligrey/FileSaver.js) – for file download  
  - [`uuid`](via `crypto.randomUUID`) – for generating unique IDs

- **Browser APIs**:  
  - `IndexedDB` – to persist project state locally  
  - `DOM` & `Events` – interactive UI  
  - `Blob`, `Date`, `localStorage` fallback via in-browser state

- **No frameworks**

## License

GPL-3.0  
See `LICENSE` or [gnu.org/licenses/gpl-3.0](https://www.gnu.org/licenses/gpl-3.0.html)
