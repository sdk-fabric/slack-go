
# slack-go

This [SDK](https://github.com/sdk-fabric/slack-go) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/slack

## Usage

```go
import (
	"github.com/sdk-fabric/slack-go/sdk"
)

var client, _ = sdk.Build("[access_token]");

// Deletes a message from a channel.
response, err := client.Chat().delete(Delete_Message_Request{})

// Retrieves a permalink URL for a specific existing message.
response, err := client.Chat().getPermalink("channel", "message_ts")

// Sends an ephemeral message to a user in a channel.
response, err := client.Chat().postEphemeral(Post_Ephemeral_Request{})

// Sends a message to a channel.
response, err := client.Chat().postMessage(Post_Message_Request{})

// Schedules a message to be sent to a channel at a future time.
response, err := client.Chat().scheduleMessage(Schedule_Message_Request{})

// Updates a message in a channel.
response, err := client.Chat().update(Update_Message_Request{})
```
