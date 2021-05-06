FROM python:alpine
RUN pip install redis && pip install requests
COPY worker.py .
 
FROM scratch
COPY --from=0 / /

CMD ["worker.py"]
ENTRYPOINT ["python"]
