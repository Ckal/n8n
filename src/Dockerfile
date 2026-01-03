# Use the official n8n Docker image
FROM docker.n8n.io/n8nio/n8n:latest

# Update system and install necessary dependencies


# Create a user to run n8n (recommended for Hugging Face Spaces)
RUN useradd -m -u 1000 user

# Set environment variables
ENV HOME=/home/user PATH=/home/user/.local/bin:$PATH N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true N8N_HOST=0.0.0.0 N8N_PORT=7860  

# Set user permissions
USER user

# Set the working directory
WORKDIR $HOME/app

# Expose the port required by Hugging Face
EXPOSE 7860

# Start n8n on container launch
CMD ["n8n"]