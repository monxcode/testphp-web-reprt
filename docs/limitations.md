# Limitations

This assessment was conducted using the WebSentinel deep-safe scan profile.  
While comprehensive within its configured scope, certain limitations apply.

## Technical Limitations

- Scan performed in safe mode (no destructive payload execution)
- No brute-force or aggressive exploitation attempts
- No authenticated user-level testing
- No business logic abuse testing
- No manual penetration testing validation
- No source code access

## Environmental Constraints

- Target environment is an intentionally vulnerable demo application
- Server-side configurations may not reflect real-world hardened systems
- False positives may exist due to automated detection logic

## Tool-Based Constraints

- CVSS scoring was approximated based on severity classification
- Some vulnerabilities may require manual verification
- Dynamic content detection depends on response behavior
- JavaScript-heavy endpoints may not be fully interpreted

## Reporting Constraints

- Findings are based strictly on scan output JSON data
- No external threat intelligence correlation applied
- No compliance mapping (e.g., OWASP Top 10, PCI-DSS) included in this report version

## Important Note

This assessment is for educational and research purposes only.  
Results should not be considered a full professional penetration test.

Manual validation and extended security testing are recommended for real-world production environments.