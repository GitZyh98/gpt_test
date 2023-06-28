FROM python:3.9
WORKDIR /qh_search

COPY deploy/requirements.txt ./
RUN pip3 install --upgrade pip -i https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install --no-cache-dir -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple


# COPY chat_gpt ./chat_gpt

COPY deploy/setup.py ./
COPY deploy ./
COPY main.py ./
COPY README.md ./
COPY static ./
COPY templates ./
RUN python setup.py develop

CMD ['python']
#ENTRYPOINT [ "sh", "-c", "python $FILE_NAME" ]
