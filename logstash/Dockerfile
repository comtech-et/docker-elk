FROM logstash:5

# Add your input logstash plugins setup here
RUN for input in cloudwatch; \
    do echo "logstash-plugin install logstash-input-$input"; \ 
    logstash-plugin install logstash-input-$input; done

# Add your output logstash plugins setup here
RUN for output in cloudwatch sns sqs; \
    do echo "logstash-plugin install logstash-output-$output"; \
    logstash-plugin install logstash-output-$output; done

# Add your filter logstash plugins setup here
