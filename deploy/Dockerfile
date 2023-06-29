FROM python:3.9
WORKDIR /qh_search

COPY deploy/requirements.txt ./
RUN pip3 install --upgrade pip -i https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install --no-cache-dir -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

COPY static ./static
COPY templates ./templates
COPY main.py ./
COPY __init__.py ./

COPY deploy/setup.py ./
EXPOSE 8080
