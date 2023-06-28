FROM python:3.9
WORKDIR /qh_search

COPY chat_gpt/deploy/requirements.txt ./
RUN pip3 install --upgrade pip -i https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install --no-cache-dir -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple


COPY chat_gpt ./chat_gpt

COPY chat_gpt/deploy/setup.py ./
RUN python setup.py develop

CMD ['python']
#ENTRYPOINT [ "sh", "-c", "python $FILE_NAME" ]
