# Steps Used to Fix the Problem
1. Verified the issue by sending a ping from Host D to Host B. The ping failed.
2. Pinged Host A from Host D to verify whether the router was configured correctly. The ping was successful.
3. Checked the IP configuration on Host B and found that the default gateway was configured, but the IP address and subnet mask were missing.
4. Configured the IP address and subnet mask on Host B.
5. Verified the fix by sending another ping from Host D to Host B. The ping was successful.