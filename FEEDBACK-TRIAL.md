# PR feedback trial

This file is a disposable fixture for testing GitHub feedback routing.

## Cleanup timing

- Each fixture keeps its original expiry time.
- Late cleanup does not restart the retention window.
- A failed deletion should be recorded and retried.
