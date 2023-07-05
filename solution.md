function firstNonRepeated(s: string): string {
  const charCount: Record<string, number> = {};

  for (const char of s) {
    charCount[char] = (charCount[char] || 0) + 1;
  }

  for (const char of s) {
    if (charCount[char] === 1) {
      return char;
    }
  }

  return "";
}
