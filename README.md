# laravel-sqs-fifo-queue

Forked from: https://github.com/shiftonelabs/laravel-sqs-fifo-queue

## Change

FIFO queues does not accept a delay per job, which the original package prevents by throwing an exception, which is good. Issue is, that in Laravel, Mailables always use delay, even if `null`, so queueing mailables in a FIFO queue was not possible.

This fork simply ignores the delay.
