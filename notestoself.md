```
@PreAuthorize("hasPermission(#pubId,1) and @titanPermissionEvaluator.isFeatureEnabled(#pubId,#pubToken,265)")
	public ResponseEntity<?> upsertCreativeTags(
			@RequestBody AutoApprovalTagRequestDTO requestDto,
	        @Param("pubToken") @RequestHeader(required = true, name = "PubToken") String pubToken,
	        @Param("pubId") @PathVariable(required = true, name = "pubId") Integer pubId,
	        @PathVariable(required = true, name = "catId") Integer catId,
	        @RequestParam(name = "siteId", defaultValue = "0") Integer siteId,
	        @Context HttpServletRequest request) {
```
without @Param pubid was null, reread marco behler blogs
