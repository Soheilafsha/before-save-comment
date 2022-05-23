# before-save-comment
Moralis
Moralis.Cloud.beforeSave("Review", (request) => {
  const comment = request.object.get("comment");
  if (comment.length > 140) {
    // Truncate and add a ...
    request.object.set("comment", comment.substring(0, 137) + "...");
  }
});
