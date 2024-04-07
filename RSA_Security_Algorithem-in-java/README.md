# RSA_Security_Algorithem-in-java
RSA Algorithem to encrypt and decrypt messages between sender and receiver using java swing  

RSA Encryption

Suppose someone wants to encrypt the plaintext 19. We thus have to calculate:

C ≡ 199 mod 1189.

This is most efficiently calculated using the Repeated Squares Algorithm:

Step 1:

C ≡ 198+1 mod 1189
C ≡ (198)(191) mod 1189

Step 2:

191 ≡ 19 mod 1189
192 ≡ 192 = 361 mod 1189
194 = (192)2 ≡ (361)2 = 130321 ≡ 720 mod 1189
198 = (194)2 ≡ (720)2 = 518400 ≡ 1185 mod 1189

Step 3:

C ≡ (198)(191) mod 1189
≡ (1185)(19) mod 1189
≡ 22515 mod 1189
≡ 1113 mod 1189

So the ciphertext C is 1113.

RSA Decryption

Suppose we now receive this ciphertext C=1113. To decrypt it we have to calculate:

M ≡ 1113249 mod 1189.

This is most efficiently calculated using the Repeated Squares Algorithm:

Step 1:

M ≡ 1113249 mod 1189
M ≡ 1113128+64+32+16+8+1 mod 1189
M ≡ (1113128)(111364)(111332)(111316)(11138)(11131) mod 1189

Step 2:

11131 ≡ 1113 mod 1189
11132 ≡ 11132 = 1238769 ≡ 1020 mod 1189
11134 = (11132)2 ≡ (1020)2 = 1040400 ≡ 25 mod 1189
11138 = (11134)2 ≡ (25)2 = 625 mod 1189
111316 = (11138)2 ≡ (625)2 = 390625 ≡ 633 mod 1189
111332 = (111316)2 ≡ (633)2 = 400689 ≡ 1185 mod 1189
111364 = (111332)2 ≡ (1185)2 = 1404225 ≡ 16 mod 1189
1113128 = (111364)2 ≡ (16)2 = 256 mod 1189

Step 3:

M ≡ (1113128)(111364)(111332)(111316)(11138)(11131) mod 1189
≡ (256)(16)(1185)(633)(625)(1113) mod 1189
≡ 2137259174400000 mod 1189
≡ 19 mod 1189

So the plaintext M is 19.
