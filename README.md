## LUCRARE DE LABORATOR 3: CI/CD AVANSAT CU GITHUB ACTIONS

### Obiective

- Înțelegerea proceselor automate de build și testare pe mai multe platforme.
- Configurarea linter-ului automat.
- Salvarea rezultatelor testelor ca artefacte.
- Crearea și integrarea unui badge de build status în proiect.

### Realizați următoarele sarcini:

1. Creați un nou repozitoriu GitHub și clonați-l local, numit Laborator3.

2. Creați două fișiere:
   - **script.py**, care afișează un mesaj simplu:

     ```python
     print("Salut, GitHub Actions extins!")
     ```

   - **test_eg.py**, care conține un test simplu:

     ```python
     def test_example():
         assert 1 + 1 == 2
     ```

3. Încărcați fișierele în repozitoriu și confirmați sincronizarea locală și remote.

4. Creați un workflow nou în `.github/workflows/` numit `python-ci.yml`, care:
   - Rulează pe Ubuntu și Windows.
   - Testează pe Python 3.8, 3.9 și 3.10.
   - Instalează flake8 și pytest.
   - Rulează linter-ul flake8 pe tot codul sursă.
   - Rulează scriptul `script.py`.
   - Rulează testele cu pytest, salvând rezultatul într-un fișier `result.log`.
   - Încarcă fișierul `result.log` ca artefact de build.

5. Verificați rularea automată a workflow-ului la fiecare push sau pull request.
