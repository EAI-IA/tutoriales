# Verificar drivers

| Nome | Tags | pasos |
|------|------|-------|
| lspci \| grep -i nvidia | | |
| pip list | | |
| pip list \| grep -E 'tensorflow\|protobuf' | | |
| Operaciones en python | | |
| almacenar the keys API | | 1. `touch .env`<br>2. OPENAI_API_KEY=tu_api_key<br>3. `pip install python-dotenv`<br>4. from dotenv import load_dotenv<br>   import os<br><br>   # Cargar las variables desde .env<br>   load_dotenv()<br><br>   # Acceder a las variables<br>   openai_api_key = os.getenv('OPENAI_API_KEY')<br>5. |