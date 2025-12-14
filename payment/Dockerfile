FROM python:3.9

WORKDIR /opt/server

# Copy dependencies and install
COPY requirements.txt .
RUN pip3 install -r requirements.txt

# Copy application code and config
COPY *.py .
COPY payment.ini .

# Expose port (optional)
EXPOSE 8080

# Correct CMD syntax
CMD ["uwsgi", "--ini", "payment.ini"]
