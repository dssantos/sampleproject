## How to Dev

1. Clone repo
2. Create a virtualenv
3. Active virtualenv
4. Install dependences
5. Copy and edit your .env file

```console
git clone https://github.com/dssantos/sampleproject.git sampleproject
cd sampleproject
python -m venv .sampleproject
source .sampleproject/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
KEY=$(python contrib/secret_gen.py)
sed -i "/^SECRET_KEY=/c\SECRET_KEY=${KEY}" .env
cat .env

```
