# Evidence-only container (no proprietary core included)
FROM python:3.12-slim

WORKDIR /app

# Copy public artifacts (docs, datasets, evidence)
COPY docs/ ./docs/
COPY datasets/ ./datasets/
COPY evidence/ ./evidence/

# Default message (container is for packaging/transport, not execution)
CMD ["python","-c","print('TCDS Omnikernel v5.8 evidence package (no runnable core). See /app/docs, /app/datasets, /app/evidence.')"]
