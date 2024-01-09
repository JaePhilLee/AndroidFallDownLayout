# AndroidFallDownLayout
FallDownLayoutAnimation for Layout View

- The two files in the path below
 : /res/anim/~.xml

- Use XML
  <~ConstraintLayout
    ...
    android:layoutAnimation="@anim/layout_animation_fall_down"/>
  
- Restart Programmatically
  public void startFallDowLayoutAnimation(final RecyclerView recyclerView) {
		final Context context = recyclerView.getContext();
		final LayoutAnimationController controller =
				AnimationUtils.loadLayoutAnimation(context, R.anim.layout_animation_fall_down);

		recyclerView.setLayoutAnimation(controller);
		recyclerView.getAdapter().notifyDataSetChanged();
		recyclerView.scheduleLayoutAnimation();
	}
