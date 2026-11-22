ZAD OSINT MUSIC — PYTHON / FLASK VERSION

PHONE SE RENDER PAR DEPLOY:

1) ZIP extract karo.
2) Extracted ZAD_OSINT_MUSIC_PYTHON folder ke andar ye cheezein hain:
   - app.py
   - requirements.txt
   - Procfile
   - render.yaml
   - static/index.html
3) GitHub app ya github.com kholo.
4) New repository banao: zad-osint-music
5) Is folder ke ANDAR ke files/folders repository ke ROOT mein upload karo.
   Dhyan: app.py repository ke root par hona chahiye; app.py ko kisi aur folder ke andar mat rakho.
6) render.com par login karo -> New + -> Web Service.
7) GitHub repository connect karo.
8) Settings:
   Runtime: Python 3
   Build Command: pip install -r requirements.txt
   Start Command: gunicorn app:app --workers 1 --threads 4 --timeout 120
   Root Directory: blank chhodo
   Instance Type: Free
9) Create Web Service / Deploy dabao.
10) Deploy ke baad Render URL kholo. Health check ke liye URL ke aage /healthz lagao.

IMPORTANT:
- App original uploaded HTML music player se bani hai; Python/Flask sirf website serve karta hai.
- Login gate ko startup par skip kiya gaya hai; account features jab zaroori hon tab login/register modal use ho sakta hai.
- Theme ka default light/white-blue hai. Agar browser mein purani theme saved ho to app ke theme toggle se light select karo.
- Songs jo browser IndexedDB/local storage mein add hote hain woh usi device/browser mein rehte hain; Render server par automatically upload/sync nahi hote.
- Render free service idle hone par sleep kar sakti hai, pehli request par start hone mein waqt lag sakta hai.
- Background music playback browser/phone ke restrictions par depend karta hai.
