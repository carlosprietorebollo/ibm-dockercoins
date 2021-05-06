FROM python:alpine
RUN pip install Flask
COPY rng.py .
 
FROM scratch
COPY --from=0 / /

CMD ["rng.py"]
ENTRYPOINT ["python"]
EXPOSE 8080
