FROM alpine:3.19

WORKDIR /app

RUN apk add --no-cache python3 py3-pip
RUN pip install --break-system-packages flask==3.0.* 

COPY hello.py .

RUN addgroup -S app && adduser -S appuser -G app

ENV FLASK_APP=hello 
EXPOSE 8000 
USER appuser
CMD ["flask", "run", "--host", "0.0.0.0", "--port", "8000"]





