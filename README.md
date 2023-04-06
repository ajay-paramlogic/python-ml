## Python Dev with VirtualEnv
```sh
# last `venv` is path for virtual environment
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn src.main:app --host 0.0.0.0 --port 80 --reload
# Choose python env in VSCode from bottom bar
```

## Adding a package and updating requirements.txt
```sh
pip install numpy matplotlib ipykernel
echo "matplotlib==$(pip freeze | grep matplotlib | awk -F '==' '{print $2}')" >> requirements.txt
```

## Clean Uninstall
```
pip freeze > installed_packages.txt
pip uninstall -y -r installed_packages.txt
rm installed_packages.txt
```