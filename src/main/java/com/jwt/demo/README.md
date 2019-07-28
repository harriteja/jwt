JWT --> transmitting information between two parties in a compact
The bits of information encoded in the body of a JWT are called claims
The expanded form of the JWT is in a JSON format, so each claim is a key in the JSON object.

JWT can be cryptographically signed (JWS) or encrypted (JWE)


JSON Web Signature (JWS) represents content secured with digital signatures or Message Authentication Codes (MACs) 
using JSON-based data structures.  Cryptographic algorithms and identifiers for use with this specification are described in the separate JSON Web Algorithms (JWA) 
specification and an IANA registry defined by that specification.  Related 
encryption capabilities are described in the separate 
JSON Web Encryption (JWE) specification.

JSON Web Encryption (JWE) represents encrypted content 
using JSON-based data structures.  Cryptographic algorithms and identifiers for use with this specification are described in the separate JSON Web Algorithms (JWA) 
specification and IANA registries defined by that specification.  Related
digital signature and Message Authentication Code (MAC) capabilities are described in the separate
JSON Web Signature (JWS) specification.


eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJKb2UifQ.ipevRNuRP6HflG8cFKnmUPtypruRC4fb1DWtoLL62SY

The first part is the header, which at a minimum needs to specify the algorithm used to sign the JWT. Eg: {"alg":"HS256"}
The second part is the body. This part has all the claims of this JWT encoded in it. Eg with single claim : { "sub": "Joe" } 
The final part is the signature. It's computed by passing a combination of the header and body through the algorithm specified in the header.
        --> To compute the signature, you need a secret key to sign it. We'll cover keys and algorithms later.
        
HMAC --> Hash based message authentication code
SHA  --> Secure Hash Algorithm

CSRF --> Cross site request forgery
