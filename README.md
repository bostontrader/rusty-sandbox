I have discovered an error whereby a test works just fine locally, but fails when run on Travis.ci.  This repo replicates that problem while dispensing with other extraneous stuff.

My present intuition is that the problem stems from an issue with actix-web and binding.

The test should goad the actix-web into binding to an unbindable address, thus causing an erroneous shutdown.  Instead, the test hangs.  This is indicative of actix-web successfully binding.
