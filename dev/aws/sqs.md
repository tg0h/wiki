# sqs

```bash
echo -n <message> | md5

# do not use this because herestrings always end with a newline
# throwing off the hash
md5<<<'a message'
```

```bash
# adding message attributes to a sqs message
  local msgAtt=$(jo -d. taskName.StringValue=event1 taskName.DataType=String \
taskNames.StringValue=event2 taskNames.DataType=String)

jq -L "~/.config/jq" "$jqQuery" <<< $result

  aws sqs send-message --queue-url $queueUrl \
    --message-body "t" \
    --message-attributes $msgAtt

```
